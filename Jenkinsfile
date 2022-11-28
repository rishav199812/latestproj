// pipeline {
//  agent any
// stages{
//         stage('Hello'){
// // 		environment {
// // 			NEW_TAG = "${git describe --tags}"
// // 			IMAGE_TAG = "${git describe ${git rev-list --tags --max-count=1}}"
// // 		}
//             steps{
//                 echo "Checking World"
// 		   sh "(script: "git describe --tags ${commit}", returnStdout: true)?.trim()"
		   
// 		echo "The current build number is ${env.NEW_TAG}"
// 		sh "${env.NEW_TAG}"
// 		echo "The current build number is ${env.IMAGE_TAG}"
// 		sh "${env.IMAGE_TAG}"
		
//             }
//         }
// }
// }
pipeline{
    agent any
    
stages{
    stage ('hello'){
        environment {
    GIT_TAG_NAME = (script: "git describe --tags")
}
        steps{
            
      echo "${env.GIT_TAG_NAME}"
        }
    }
    }
}
