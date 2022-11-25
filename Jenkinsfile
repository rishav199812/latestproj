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
                     script{
	            when { tag "demo-*" }
                    zip archive: true, dir: 'tests', glob: '', zipFile: 'tests.zip'
                }
                    echo "Deploying Lambda"
		        }
	}
    }
}
