pipeline {
	agent any
	stages {
	    stage ('clean up') {
	        steps {
	            cleanWs()
	        }
	    }
	    
	    stage ('clone') {
			steps {
				sh 'git clone https://github.com/sunilnl18/Git-Project1.git'
			}
	    }
		stage ('build') {
			steps {
			    dir ('Git-Project1'){
				    echo "Hello Sunil"
				    sh 'mvn clean install -DskipTests'
			    }
			}
		
		}
		stage ('test') {
			steps {
			    dir ('Git-Project1') {
				    sh 'mvn test'
			    }
      }
    }
  }
}
