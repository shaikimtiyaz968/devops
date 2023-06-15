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
                bat 'docker-compose down Dockerfile'
            } 
        }
        stage('Docker start') {
            steps {
                bat 'docker-compose -d up'
            }
        }
       
    }
}
