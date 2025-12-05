pipeline {
    agent {
		docker {
			image "ruby:3.4.7"
		}
	}

	options {
		timeout(time: 1, unit: "HOURS")
	}

    stages {
        stage("build") {
			options {
				timestamps()
			}

            steps {
				sh "ruby --version"
            }
        }
	}

	post {
		always {
			echo "Always !"
		}

		success {
			echo "Success !"
		}
	}
}
