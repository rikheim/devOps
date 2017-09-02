pipeline {
	agent any

	stages{
		stage('build'){

			agent{
				label 'slave'		
			}
			tools{
				jdk "JDK 8"
				maven "appache-maven-3.3.9"
			}
			steps {
				sh('mvn clean install')		
			}
		}

	}
		

	post {
		always{
			notification currentBuild.result	
		}	
	}
}
