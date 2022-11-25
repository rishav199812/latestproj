pipeline {
 agent any
stages{
        stage('Hello'){
            steps{
                echo "Checking World"
                echo "$env"
                echo "$env.change_id"
                echo "$env.target_id"
                echo "$env.GIT_TAG_MESSAGE"
            }
        }
}
}
