pipeline {
	agent any
	
	stages {
		
		stage ('build') {
			steps {
				sh 'cd node'
				sh 'npm install'
				sh 'echo "Build"'
			}
		}
		stage ('Unit Test') {
			steps {
                                sh 'cd node'
				/*sh 'npm test'*/
				sh 'echo "Unit Test"'
                        }
                }		
		stage ('SonarQube') {
			environment {
				scannerHome = tool 'SonarQubeScanner'
			}			
			steps {
				withSonarQubeEnv('SonarQube') {
					sh "${scannerHome}/bin/sonar-scanner"
					sh 'echo "SonarQube"'
				}
                                
                        }
                }
	}
}
