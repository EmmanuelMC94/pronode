pipeline {
	agent any
	
	stages {
		stage ('move') {
			steps {
				sh 'cd node'
				sh 'echo "moving to node folder"'
			}
		}
		stage ('build') {
			steps {
				sh 'npm install'
				sh 'echo "Build"'
			}
		}
		stage ('Unit Test') {
			steps {
                                /*sh 'npm test'*/
				sh 'echo "Unit Test"'
                        }
                }
		stage ('Move2'){
			steps{
				sh 'pronode'
				sh 'echo"moving to pronode folder"'
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
