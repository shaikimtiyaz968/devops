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
                sh 'docker build -t ubuntu_j .'
            }
        }
        stage('Tag Image') {
            steps {
               sh 'docker tag ubuntu_j:latest shaikimtiyaz968/ubuntu_j:latest'
            }
        }
        stage('Push Image') {
            steps {
                sh 'docker login -u shaikimtiyaz968 -p 9182478469'
                sh 'docker push ubuntu_j:latest'
            }
        }
    }
}
