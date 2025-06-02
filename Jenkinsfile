pipeline{
	agent any
	tools{
		maven 'Maven'
	}
	stages{
		stage('Checkout'){
			steps{
				git branch : 'main' , url : 'https://github.com/Nischay2004/maven-hello-world.git'
			}
		}
		stage('Build') {
			steps{
				sh 'mvn clean package'
			}
		}
		stage('Test') {
			steps {
				sh 'mvn test'
			}
		}
		
		stage('Run Application'){
			steps {
				sh 'mvn exec:java -Dexec.mainClass=com.example.App'
			}
		}
	}
	
