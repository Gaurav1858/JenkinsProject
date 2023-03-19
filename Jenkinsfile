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
        post {
           failure {
               mail to: team@example.com, subject: ‘The Pipeline failed :(‘
        }
      }
    }
}
