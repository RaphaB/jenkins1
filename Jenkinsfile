pipeline {
    agent {
		docker {
			image "ruby:3.4.7"
		}
	}

	triggers {
		pollSCM("* * * * *")
	}

	options {
		timestamps()
	}

	stages {
        stage("build") {
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
