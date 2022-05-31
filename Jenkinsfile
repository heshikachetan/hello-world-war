pipeline {
	agent {label 'slave2'}
    			stages {
        			stage('Checkout') {
            				steps {
					sh "rm -rf /var/lib/jenkins/workspace/pipeline1/hello-world-war"	
               				 sh "git clone https://github.com/heshikachetan/hello-world-war.git"
            					}
       					 }
				stage('Build') {
            				steps {
               				 sh "cd hello-world-war"
						sh "docker build -t heshikachetan/hello:1.0 ."
            					}
       					 }
				stage('Publish') {
					steps {
						sh "docker login -u heshikachetan -p Chetan@1987'\$'"
						sh "docker push heshikachetan/hello:1.0"
					}
				}
				/*stage('Deploy') {
            				steps {
						sh "pwd"
						sh "ls"
						sh "whoami"
						echo "test"
               				 sh "cp /var/lib/jenkins/workspace/pipeline1/target/hello-world-war-1.0.0.war /opt/apache-tomcat-9.0.62/webapps/"
            					}
       					 }*/
   				 }
		}
