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
                sh '''npm --verison
                      node --version
                     npm ci
                     npm run build
                '''
            }
        }
    }
}
