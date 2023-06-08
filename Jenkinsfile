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
                bat 'docker build -t ubuntu_j .'
            }
        }
        stage('Tag Image') {
            steps {
               bat 'docker tag ubuntu_j:latest shaikimtiyaz968/ubuntu_j:latest'
            }
        }
        stage('Push Image') {
            steps {
                bat 'docker login -u shaikimtiyaz968 -p 9182478469'
                bat 'docker push shaikimtiyaz968/ubuntu_j:latest'
            }
        }
    }
}
