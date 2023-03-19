pipeline {
    agent any

    stages {
        stage ('Build') {
            steps {
                sh 'javac Hello2.java'
                sh 'java Hello2'
                echo "Build Successful."
            }
        }
    }
    post {
           failure {
               emailext attachLog:true, bcc: '', body: 'Pipeline is failed!', cc: '', from: '', replyTo: '', subject: 'post Build Action Email', to: 'gaurav.shukla@knoldus.com'
        }
      }
}
