pipeline {
  agent any
    stages {
	stage('Deploy Lambda') {
                steps {
             		 echo "Zipping folder"
                     script{
                    zip archive: true, dir: 'fetch_from_S3', glob: '', zipFile: 'fetch_from_S3.zip'
                }
            		echo "Deploying Lambda"
			        //sh "aws lambda update-function-code --function-name ${params.Lambda}-${params.Environment} --zip-file fileb://fetch_from_S3.zip"
		        }
	}
   }
}
