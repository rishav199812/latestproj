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
		when { tag "demo-*" }
                steps {
             		 echo "Zipping folder"
                     script{
                    zip archive: true, dir: 'demotst', glob: '', zipFile: 'demotst.zip'
                }
                    echo "Deploying Lambda"
		        }
	}
    }
}
