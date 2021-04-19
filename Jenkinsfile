pipeline {
	agent any
	
	stages {
		stage ('Complile Stage') {
			
			steps {
				withMaven(maven: 'maven_3_6_3') {
					sh 'mvn clean compile'
				}
			}
		}
		stage ('Testing Stage'){
			steps {
				withMaven(maven: 'maven_3_6_3') {
					sh 'mvn test'
				}
			}
		}
		stage ('Deployment Stage'){
			steps {
				withMaven(maven: 'maven_3_6_3') {
					sh 'mvn depoy'
				}
			}
		}
	}
	
}	
