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
                bat 'docker build -t nginx_j .'
            } 
        }
        stage('Tag Image') {
            steps {
               bat 'docker tag nginx_j:latest shaikimtiyaz968/alpine_j:latest'
            }
        }
        stage('Run Image') {
            steps {
              
                bat 'docker stop nginx_j'
            }
        }
        stage('Push Image') {
            steps {
                bat 'docker login -u shaikimtiyaz968 -p 9182478469'
                bat 'docker push shaikimtiyaz968/alpine_j:latest'
            }
        }
    }
}
