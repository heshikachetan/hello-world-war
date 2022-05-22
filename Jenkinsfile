pipeline {
	agent { label 'slave3' }
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
				stage('Deploy') {
            				steps {
               				 sh "cp hello-world-war-1.0.0.war /opt/apache/tomcat-9.0.62/webapps/"
            					}
       					 }
   				 }
		}
