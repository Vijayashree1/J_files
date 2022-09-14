pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
				sh '''
				 mvn clean install
				'''
			}
		}
	stage('deploy') {
	    steps {
				sh '''
				 cp /root/var/lib/jenkins/workspace/pipeline_demo/target/*.jar /root/opt/apache-tomcat-8.5.82/webapps/
				'''
			}
		}
    }
}
