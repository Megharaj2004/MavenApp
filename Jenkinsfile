pipeline{
	agent any
	tools{
		jdk 'jdk'
		maven 'maven'
	}
	stages{
		stage('Checkout'){
		  steps{
		    git branch: 'master', url: 'https://github.com/Megharaj2004/MavenApp'
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
		stage('Run application'){
		  steps{
		    sh 'java -cp target/MavenApp-1.0-SNAPSHOT.jar com.example.App'
		  }
		}
	}
