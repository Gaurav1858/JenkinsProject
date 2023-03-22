pipeline {
    agent any

    stages {
    	stage ('Production') {
    	    steps {
    	        echo "Deployment Successful."
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
