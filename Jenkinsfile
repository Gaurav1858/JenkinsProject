pipeline {
    agent any

    stages {
    	stage ('Build') {
    	    steps {
    	        sh 'cat README.MD'
    	        echo "Build Successful."
    	    }
    	}
        post {
          failure {
            mail bcc: '', body: 'test email for pipeline.', cc: '', from: '', replyTo: '', subject: 'Test Email', to: 'gaurav.shukla@knoldus.com'
         }
       }
    }
}
