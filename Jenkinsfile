pipeline {
    agent any
    
    stages {
    	stage ('Build') {
    	    steps {
    	        sh '''
                    javac Hello.java
    	            java Hello 
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
