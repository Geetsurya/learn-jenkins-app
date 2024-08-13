pipeline {
    agent any

    stages {
 
        stage('with docker'){
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps{
                sh ''' echo "surya"       
                '''
            }
        }

        stage('deploy'){
            agent{
                docker{
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps{
                sh '''
                    npm install netlify-cli -g
                    netlify --version
                '''
            }
        }
    }
}
