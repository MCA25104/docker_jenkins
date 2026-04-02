pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git uri:'https://github.com/MCA25104/docker_jenkins.git',branch:'main'
            }
        }
      stage('Build Image'){
        steps{
            bat 'docker build -t mywebsite.'
        }
    }
        stage('Stop Old Container'){
            steps {
                bat 'docker stop mycont || exit 0'
                bat 'docker rm mycont || exit 0'
            }
        }
        stage ('Run Image - Containerize'){
            steps{
                bat 'docker run -d -p 7000:80 --name mycont mywebsite'
            }
        }
    }
}
