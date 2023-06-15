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
                bat 'docker-compose up'
            }
        }
       
    }
}
