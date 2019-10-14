pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'run this stage - only if the branch = master branch'
            }
        }
        stage('Test on Linux') {
            steps {
                sh 'uname -a'
            }
        }
        stage('Test on Windows') {
            steps {
                echo "We are currently working on branch: ${env.BRANCH_NAME}"
                sh 'echo $env.BRANCH_NAME'
            }
        }
    }
}
