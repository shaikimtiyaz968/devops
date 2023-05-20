pipeline {
    agent any
    environment{
        microcare ='academy'
        devops ='customvariables'
    }
     stages {
        stage('Build') {
            steps {
                echo '${USER}'
                //  sh "printenv | sort"
            }
        }
        stage('Build1') {
            steps {
                echo '${microcare}'
                echo '${devops}'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploying'
            }
        }
    }
}
