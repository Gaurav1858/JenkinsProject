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
        post {
          failure {
            mail to: uploadyourbrain18@gmail.com, subject: ‘The Pipeline failed :(‘
        }
      }
    }
}
