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
// pipeline{
//     agent any
    
// stages{
//     stage ('hello'){
//         //environment {
//     //GITES_TAG_NAME = sh(script: "git describe --tags")
// 		//TAG = "${GIT_TAG_NAME}"
//}
//         steps{
            
//       echo "${env.TAG}"
// 		echo "${env.GIT_TAG_NAME}"
// 		echo "${GIT_TAG_NAME}"
//         }
//     }
//     }
// }
pipeline{
agent any
stages {
stage("Get dir size") {
    steps {
   sh "mv son tcone"
	    script {
	    fileOperations ([folderRenameOperation(String source: 'tcone', String destination: 'democheck')])
	    }
    }
  }
}
}
