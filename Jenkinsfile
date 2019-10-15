pipeline {
    agent none
    stages {
        stage('Build') {
            if(env.BRANCH_NAME == 'develop')
            {
                agent { label 'develop' }
                steps {
                    sh 'echo Its develop'
                }
            }
        }
        stage('Build') {
            if(env.BRANCH_NAME == 'test')
            {
                agent { label 'test' }
                steps {
                    sh 'echo Its test'
                }
            }
        }
        stage('Build') {
            if(env.BRANCH_NAME == 'stage')
            {
                agent { label 'stage' }
                steps {
                    sh 'echo Its stage'
                }
            }
        }
    }
}
