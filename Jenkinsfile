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
                                sh 'npm test'
				sh 'echo "Unit Test '
                        }
                }
		stage ('Sonarqube') {
			
			steps {
                                sh 'echo "SonarQube"'
                        }
                }
	}
}
