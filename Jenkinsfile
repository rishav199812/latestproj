pipeline{
    agent { label 'docker' }
        docker { image 'python:3' }
    }
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
        stage ('test'){
            steps{
                sh "pwd"
                sh "pip --version"
                sh "pip install --user -r requirements.txt"
                sh "pytest ./tests/test_data.py"
            }
        }
    }
}