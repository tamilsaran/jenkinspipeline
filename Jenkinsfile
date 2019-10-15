pipeline {
    agent any
    stages {
        stage('test3') {
            steps {
                script {
                    if (env.BRANCH_NAME == 'develop') {
                        echo 'I only execute on the master branch'
                    } else {
                        echo 'I execute elsewhere'
                    }
                }
            }
        }
    }
}
