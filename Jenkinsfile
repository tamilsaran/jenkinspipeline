pipeline {
    agent none
    stages {
        stage('Develop') {
            agent { label 'develop' }
            steps {
                script {
                    if (env.BRANCH_NAME == 'master') {
                        echo 'I only execute on the develop'
                        sh 'mkdir dev'
                    } else {
                        echo 'I execute elsewhere'
                    }
                }
            }
        }
        stage('Test') {
            agent { label 'test' }
            steps {
                script {
                    if (env.BRANCH_NAME == 'master') {
                        echo 'I only execute on the Test'
                        sh 'mkdir test'
                    } else {
                        echo 'I execute elsewhere'
                    }
                }
            }
        }
        stage('Stage') {
            agent { label 'stage' }
            steps {
                script {
                    if (env.BRANCH_NAME == 'master') {
                        echo 'I only execute on the stage'
                        sh 'mkdir stage'
                    } else {
                        echo 'I execute elsewhere'
                    }
                }
            }
        }
    }
}
