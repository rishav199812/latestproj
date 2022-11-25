pipeline{
    agent any
    stages{
        stage('Hello'){
            steps{
                echo "Checking World"
            }
        }
        stage('World'){
            steps{
                echo "Second Stage"
            }
        }
        stage('Deploy Lambda') {
		//when { tag "demo-*" }
		when { tag pattern: '^mergify-*', comparator: "REGEXP" }
                steps {
                     script{
                    zip archive: true, dir: 'merg', glob: '', zipFile: 'merg.zip'
                }
            }
        when { tag pattern: '^sonar-*', comparator: "REGEXP" }
               steps {
                     script{
                    zip archive: true, dir: 'son', glob: '', zipFile: 'son.zip'
                }
            }
    }
}
}
