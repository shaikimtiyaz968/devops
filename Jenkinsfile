pipeline {
    agent any
    stages{
        stage('check out') {   
            steps {
                checkout scm 
            }
    }
  
      stage('Build Image') {
            steps {
                sh 'docker build -t node:8.11-slim Dockerfile13'
            } 
        }
        stage('Tag Image') {
            steps {
               bat 'docker tag node:8.11-slim shaikimtiyaz968/node:8.11-slim'
            }
        }
        stage('Run Image') {
            steps {
              
                bat 'docker run --name node:8.11-slim -p 2023:80 node:8.11-slim'
            }
        }
   
    }
}
