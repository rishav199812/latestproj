pipeline {
 agent any
stages{
        stage('Hello'){
		environment {
			IMAGE_TAG="$(git describe --tags `git rev-list --tags --max-count=1` | sed 's/v//g')"
		}
            steps{
                echo "Checking World"
		echo "The current build number is ${env.IMAGE_TAG}"
		sh "${env.IMAGE_TAG}"
                echo "$env.change_id"
                echo "$env.target_id"
                echo "$env.GIT_TAG_MESSAGE"
            }
        }
}
}
