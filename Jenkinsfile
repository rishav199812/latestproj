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
                steps {
             		 echo "Zipping folder fetch_from_S3/fetch_from_S3.py"
			zip archive: true, dir: 'tests', glob: '', zipFile: 'tests.zip'
                     script{
                    zip archive: true, dir: 'tests', glob: '', zipFile: 'tests.zip'
                }
                // script{ 
                // unzip zipFile: 'fetch_from_S3.zip' , dir: 'fetch_from_S3'
                // }
                sh "pwd"
                sh "ls -la"
                     //zip zipFile: 'fetch_from_S3.zip', archive: false, dir: 'fetch_from_S3'
             		 //sh "zip -r fetch_from_S3.zip fetch_from_S3 "
            		echo "Deploying Lambda"
			        //sh "aws lambda update-function-code --function-name ${params.Lambda}-${params.Environment} --zip-file fileb://fetch_from_S3.zip"
		        }
	}
    }
}
