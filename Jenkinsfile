pipeline {
    agent { label 'hawksighttest' }
    stages {
        stage('Build') {
            steps {
                echo 'run this stage - only if the branch = test branch'
            }
        }
        stage('Test on Linux') {
            steps {
                sh 'pwd'
            }
        }
        stage('Test on Windows') {
            steps {
                sh 'ip a'
            }
        }
    }
}
