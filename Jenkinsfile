//def agentLabel
//if (env.BRANCH_NAME == 'test')  {
  //  agentLabel = "hawksighttest"
//} else {
  //  agentLabel = "none"
//}

//pipeline {
   // agent { label agentLabel }
   // stages {
      //  stage('Build') {
       //     steps {
       //         script {
      //              if (env.BRANCH_NAME == 'test') {
      //                  echo "Def worked"
      //              } else {
     //                   echo 'Branch Not Found'
    //                }
   //             }
  //          }
 //       }
 //   }
//}

pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    if (env.BRANCH_NAME == 'master') {
                        sshPublisher(
                            publishers: [
                                sshPublisherDesc(
                                configName: "hawksighttest",
                                transfers: [
                                sshTransfer(
                                    execCommand: "cd /home/ubuntu/hwk-srm-frontend/;pwd"
                                ),
                                sshTransfer(
                                    execCommand: "pwd"
                                )
                            ])
                        ])
                    } else {
                        echo 'Branch Not Found'
                    }
                }
            }
        }
    }
}