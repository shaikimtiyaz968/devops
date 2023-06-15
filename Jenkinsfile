pipeline {
    agent any
    stages{
        stage('check out') {   
            steps {
                checkout scm 
            }
    }
  
      stage('Docker down') {
            steps {
                bat 'docker-compose down'
            } 
        }
        stage('Docker start') {
            steps {
                bat 'docker-compose up -d'
            }
        }
                stage('Push image') {
                    steps {
                        bat 'docker login -u shaikimtiyaz968 -p 9182478469'
                        bat 'docker push shaikimtiyaz968/nginxbuild'

            }
        }
       
    }
}
