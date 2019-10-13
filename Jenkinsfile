pipeline {
    agent none
    stages {
        stage('Build') {
            agent {
                label 'test'
            }
            when {
                expression {
                    return env.BRANCH_NAME == null;
                }
            }
            steps {
                echo 'run this stage - ony if the branch = master branch'
            }
        }
        stage('Test on Linux') {
            when {
                anyOf {
                    branch 'master'; branch 'develop'
                }
            }
            agent { 
                label 'test'
            }
            steps {
                sh 'uname -a'
            }
        }
        stage('Test on Windows') {
            agent {
                label 'test'
            }
            steps {
                echo "We are currently working on branch: ${env.BRANCH_NAME}"
                sh 'echo $env.BRANCH_NAME'
            }
        }
    }
}
