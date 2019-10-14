pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'only if the branch = master branch = 7'
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
