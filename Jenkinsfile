pipeline {
    node {
    git url: 'https://github.com/rishav199812/latestproj'
    env.GIT_TAG_NAME = gitTagName()
    env.GIT_TAG_MESSAGE = gitTagMessage()
}

stages{
        stage('Hello'){
            steps{
                echo "Checking World"
                echo "$env.change_id"
                echo "$env.target_id"
                echo "$env.GIT_TAG_MESSAGE"
            }
        }
}
}
