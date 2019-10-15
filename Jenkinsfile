pipeline {
    agent none
    stages {
        stage('test3') {
            steps {
                script {
                    if (env.BRANCH_NAME == 'master') {
                        agent { label 'develop' }
                        echo 'I only execute on the develop branch'
                    } else {
                        echo 'I execute elsewhere'
                    }
                }
            }
        }
    }
}
