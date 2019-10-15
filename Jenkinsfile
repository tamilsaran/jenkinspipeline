def agentLabel
if (env.BRANCH_NAME == 'master')  {
    agentLabel = "test"
} else {
    agentLabel = "test"
}


pipeline {
    agent none
    stages {
        stage('Develop') {
            agent { label agentLabel }
            steps {
                script {
                    if (env.BRANCH_NAME == 'master') {
                        echo "Def worked"
                    } else {
                        echo 'Branch Not Found'
                    }
                }
            }
        }
        stage('Test') {
            agent none
            steps {
                script {
                    if (env.BRANCH_NAME == 'master') {
                       echo "Got wrong"
                    } else {
                        echo 'Branch Not Found'
                    }
                }
            }
        }
        stage('Stage') {
            agent none
            steps {
                script {
                    if (env.BRANCH_NAME == 'stage') {
                        sh 'docker ps -q | xargs -r docker kill'
                        sh 'docker images -f dangling=true -q | xargs -r -n1 docker rmi -f'
                        sh 'docker-compose rm -f -v'
                        sh 'git pull && docker-compose up --build -d'
                    } else {
                        echo 'Branch Not Found'
                    }
                }
            }
        }
    }
}
