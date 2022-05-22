pipeline {
    			agent any
    			stages {
        			stage('Checkout') {
            				steps {
               				 sh "git clone https://github.com/PoojashreeSantosh/hello-world-war.git"
            					}
       					 }
				stage('Build') {
            				steps {
               				 sh "mvn clean package"
            					}
       					 }
   				 }
		}
