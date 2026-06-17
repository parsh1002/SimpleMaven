pipeline {
	agent any 
	tools{
	maven 'Maven'
	}
	
	stages{
	stage('Checkout'){
	steps{
	git branch : 'main', url : 'https://www.github.com/parsh1002/SimpleMaven.git'
	}
	}
	stage('Build'){
	steps{
	sh 'mvn clean package'
	}
	}
	stage('Test'){
	steps{
		sh 'mvn test'
	}
	}
	
	stage('Run Application'){
	steps{
	sh 'java -jar target/SimpleMaven-1.0-SNAPSHOT.jar'
	}
	}
	
	post{
	success{
	echo 'Build successful'
	}
	failure{
	echo 'build failed'
	}
	}
	}
	
	

         
	
	
