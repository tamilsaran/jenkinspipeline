pipeline {
    agent none
    stages {
        stage('test3') {
            agent { label 'develop' }
            steps {
                script {
                    if (env.BRANCH_NAME == 'master') {
                        echo 'I only execute on the develop branch'
                    } else {
                        echo 'I execute elsewhere'
                    }
                }
            }
        }
    }
}
