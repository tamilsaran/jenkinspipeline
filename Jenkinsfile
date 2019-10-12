pipeline {
    agent none
    stages {
        stage('Build') {
            agent {
                label 'test'
            }
            steps {
                checkout scm
                sh 'pwd'
            }
        }
        stage('Test on Linux') {
            agent { 
                label 'test'
            }
            steps {
                sh 'uname -a'
            }
        }
        stage('Test on Windows') {
            agent {
                label 'windows'
            }
            steps {
                unstash 'app'
                bat 'make check' 
            }
            post {
                always {
                    junit '**/target/*.xml'
                }
            }
        }
    }
}
