pipeline {
    agent {
		docker {
			image "ruby:3.4.7"
		}
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

		stage("deployment") {
			input {
				message "Voulez-vous mettre en prod ?"
				ok "Déployer"
				submitter "admin,devops"
				submitterParameter "USER_SUBMIT"
				parameters {
					string(name: "VERSION", defaultValue: "latest", description: "La version")
					booleanParam(name: "SUPER", defaultValue: true, description: "Super ?")
				}
			}

			steps {
				echo "user: ${USER_SUBMIT}"
				echo "version: ${VERSION}"
				echo "super: ${SUPER}"
				echo "Deploying !"
			}
		}
	}
}
