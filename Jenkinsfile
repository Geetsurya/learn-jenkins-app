pipeline {
    agent any

    stages {
        stage('with out docker') {
            steps {
                sh '''echo "without docker" 
                      ls -la
                      touch contsiner-no.txt
                '''
            }
        }
        
        stage('with docker'){
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps{
                sh '''echo "with docker" 
                      ls -la
                      touch contsiner-yes.txt
                '''
            }
        }
    }
}
