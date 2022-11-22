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
        stage ('test'){
            steps{
                sh "pwd"
                sh "pip install --user -r requirements.txt"
                sh "pytest ./tests/test_data.py"
            }
        }
    }
}