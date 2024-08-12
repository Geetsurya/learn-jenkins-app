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
                sh '''
                    npm ci
                    npm run build
                '''
            }
        }

        stage('test'){
            steps{
                sh ' cd build'
                sh ' test -f index.html'
    }
}
