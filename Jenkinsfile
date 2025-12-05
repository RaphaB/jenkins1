pipeline {
    agent {
		docker {
			image "ruby:3.4.7"
			label "my_ruby"
		}
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
