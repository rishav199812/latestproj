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
                steps {
             		 echo "Zipping folder fetch_from_S3/fetch_from_S3.py"
                     script{
                    zip archive: true, dir: 'demotest', glob: '', zipFile: 'demotest.zip'
                }
                    echo "Deploying Lambda"
		        }
	}
    }
}
