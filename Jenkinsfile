pipeline {
    agent any

    stages {
        stage ('Build') {
            steps {
                echo "In Development Environment"
                sh '''
                    javac Hello2.java
                    java Hello2
                    '''
                echo "Build Successful."
            }
        }
    }
    post {
           failure {
               emailext attachLog:true, body: 'Pipeline is failed!', subject: 'Post Build Action Email', to: 'gaurav.shukla@knoldus.com'
        }
           success {
               emailext attachLog:true, body: 'Pipeline is successful!', subject: 'Post Build Action Email', to: 'gaurav.shukla@knoldus.com'
        }
      }
}
