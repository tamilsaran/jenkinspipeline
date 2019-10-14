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
                sh 'date'
            }
        }
        stage('Test on Windows') {
            steps {
                sh 'ip a'
            }
        }
    }
}
