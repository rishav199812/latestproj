pipeline{
    agent any
    stages{
        stage('Hello'){
            steps{
                echo "Checking World"
		 echo "The build number is ${env.TAG_NAME}"
		    script {
		 sh(returnStdout: true, script: "git tag --sort version:refname | tail -1").trim()
		    }
            }
        }
        stage('World'){
            steps{
                echo "Second Stage"
            }
        }
        stage('Deploy Lambda') {
            parallel {
                stage ('merg'){
		when { tag pattern: '^mergify-*', comparator: "REGEXP" }
                steps {
                     script{
                    zip archive: true, dir: 'merg', glob: '', zipFile: 'merg.zip'
                }
            }
                }
                 stage ('son'){
              when { tag pattern: '^sonar-*', comparator: "REGEXP" }
               steps {
                     script{
                    zip archive: true, dir: 'son', glob: '', zipFile: 'son.zip'
                }
               }
            }
        }
    }
}
}
