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
    }
}
