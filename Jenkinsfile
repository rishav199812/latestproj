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
                sh "pytest ./tests/test_data.py"
            }
        }
    }
}