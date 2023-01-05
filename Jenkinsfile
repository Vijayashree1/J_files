pipeline {
    agent any
    stages {
        stage('Git Checkout') {
            steps {
                git 'https://github.com/Vijayashree1/J_files.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
	stage ('Deploy') {
	    steps {
		sshagent(['Deploy']) {
    		sh 'scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/Hello World/target/org.jacoco.examples.maven.java-1.0-SNAPSHOT.jar ec2-user@54.95.101.195:/opt/apache-tomcat-8.5.84/webapps'
		}
    	    }
	}
    }
}
