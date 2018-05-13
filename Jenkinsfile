pipeline {
    agent any
    stages {
        stage('Build') {
             steps {
                  echo 'Building'
                  sh 'make'
                  archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
             }
        }
        stage('Test') {

              steps {
                   echo 'Testing...'
              }
        }
        stage('Deploy') {

              steps {
                   echo 'Deploying...'
              }
        }
     }
    post {
        always {
            sh 'make'
        }
        failure {
            mail to: meetshubham05@yahoo.co.in, subject: 'The Pipeline failed :('
}
