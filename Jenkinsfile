pipeline {
    agent any
    stages {
        stage('Clone-Repo') {
	    	steps {
	        	checkout scm
	    	}
        }
	stage('Build') {
		steps {
			sh 'mvn install'
		}
	}	
 
        stage('Deployment') {
	   steps {
		sh 'scp target/gamutkart.war root@172.31.82.203:/root/distroys/apache-tomcat-9.0.91/webapps'
	}
    }
}
}
