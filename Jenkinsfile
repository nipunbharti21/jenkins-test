pipeline {
	agent any

	stages {
		stage('Build') {
			steps {
				sh 'rm -rf node_modules && npm install'
			}
		}

		stage('Test') {
			steps {
				sh 'npm run test'
			}
		}
	}
}