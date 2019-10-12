pipeline {
    agent none
    stages {
        stage('Build') {
            when {
                anyOf {
                    branch 'master'; branch 'develop'
                }
            }
            agent {
                label 'test'
            }
            steps {
                checkout scm
                sh 'pwd'
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
                sh 'echo Done'
            }
        }
    }
}
