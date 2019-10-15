def agentLabel
if (env.BRANCH_NAME == 'master')  {
    agentLabel = "test"
} else {
    agentLabel = "none"
}


pipeline {
    agent { label agentLabel }
    stages {
        stage('Build') {
            steps {
                script {
                    if (env.BRANCH_NAME == 'test') {
                        echo "Def worked"
                    } else {
                        echo 'Branch Not Found'
                    }
                }
            }
        }
    }
}
