pipeline {
	agent any 
	parameters {
		choice(name: 'ENVIRONMENT', choices: ['QA','UAT'], description: 'Pick Environment value')
	}/home/owaiss/Documents/devopsoftware/apache-tomcat-9.0.84/webapps
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/guru/slaveDD2/apache-maven-3.9.0/bin/mvn install'
	                 }}
		stage('Deployment'){
		   steps {
		sh 'cp target/seva.war /home/owaiss/Documents/devopsoftware/apache-tomcat-9.0.84/webapps'
			}}	
}}
