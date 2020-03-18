pipeline {
	agent any
	cd node
	stages {
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
