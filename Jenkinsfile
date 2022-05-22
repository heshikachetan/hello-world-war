pipeline {
	agent any
    			stages {
        			stage('Checkout') {
            				steps {
					sh "rm -rf /var/lib/jenkins/workspace/pipeline1/hello-world-war"	
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
