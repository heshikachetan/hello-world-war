pipeline {
	agent { label 'slave2' }
    			stages {
        			stage('Checkout') {
            				steps {
					sh "rm -rf /home/slave2/workspace/pipeline1/hello-world-war"	
               				 sh "git clone https://github.com/heshikachetan/hello-world-war.git"
            					}
       					 }
				stage('Build') {
            				steps {
               				 sh "mvn clean package"
            					}
       					 }
				stage('Deploy') {
            				steps {
						sh "pwd"
						sh "ls"
						sh "whoami"
						echo "test"
               				 sh "cp /home/slave2/workspace/pipeline1/target/hello-world-war-1.0.0.war /opt/apache-tomcat-9.0.62/webapps/"
            					}
       					 }
   				 }
		}
