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
            mail to: team@example.com, subject: ‘The Pipeline failed :(‘
         }
       }
    }
}
