pipeline {
    agent any

    stages {
    	stage ('Build') {
    	    steps {
    	        sh " javac Hello.java "
    	        sh " java Hello "
    	        echo "Build Successful."
    	    }
    	}
    }
    post {
          failure {
            mail bcc: '', body: 'test email for pipeline.', cc: '', from: '', replyTo: '', subject: 'Test Email', to: 'gaurav.shukla@knoldus.com'
        }
      }
}
