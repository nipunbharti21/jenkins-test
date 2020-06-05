pipeline {
	agent any

	stages {
		stage("Build") {
			steps {
				sh "rm -rf node_modules && npm install"
			}
		}

		stage("Test") {
			steps {
				sh "npm run test"
			}
		}

		stage("Completion") {
			steps {
				echo "Build result: ${currentBuild.currentResult} for ${currentBuild.projectName} and it was triggered because of this push!"
			}
		}

		stage("Check") {
			steps {
				sh "printenv"
			}
		}
	}
}