pipeline {
    agent { label 'demotest' }
    stages {
        stage('Build') {
            steps {
                echo 'run this stage - only if the branch = test branch'
            }
        }
        stage('Test on Linux') {
            steps {
                sh 'uname -a'
            }
        }
        stage('Test on Windows') {
            steps {
                sh 'ip a'
            }
        }
    }
}
