pipeline {
    agent any

	tools {
		maven 'maven'
	}

//	environment {
//		M2_INSTALL = "/usr/share/maven/bin/mvn"
//	}

    stages {
		stage('Clone-Repo') {
			steps {
				checkout scm
			}
		}
		stage('Build') {
	    	steps {
				sh 'mvn install -DskipTests'
			}
	    }
		stage('Unit Tests') {
			steps {
				sh 'mvn surefire:test'
			}
		}
		stage('Deployment') {
	    	steps {
				sh 'sshpass -p "mavvvvvv" scp target/gamutkart.war sudheer@192.168.43.21:/home/sudheer/Downloads/apache-tomcat-7.0.96.zip/webapps'
				
	    	}
		}
    }
}
