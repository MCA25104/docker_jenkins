pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/MCA25104/docker_jenkins.git'
            }
        }
      stage('Publish'){
        steps{
          publishHTML([
            allowMissing:true,
            alwaysLinkToLastBuild:false,
            keepAll:false,
            reportDir:'.',
            reportFiles:'index.html',
            reportName:'My HTML Pipe Publish'
           ])
        }
     }
    }
}
