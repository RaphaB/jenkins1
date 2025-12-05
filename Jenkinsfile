pipeline {
    agent {
		docker {
			image "ruby:3.4.7"
		}
	}

	options {
		timestamps()
	}

	parameters {
		string(name: "NAME", defaultValue: "M. Jenkins", description: "Le nom de l'agent")
		text(name: "TEXT", defaultValue: "My text", description: "Un texte")
		booleanParam(name: "TOGGLE", defaultValue: true, description: "True or False")
		choice(name: "CHOICE", choices: ["a", "b", "c", "d"], description: "Liste de choix")
		password(name: "PASSWORD", description: "Mot de passe")
	}

	stages {
        stage("build") {
            steps {
				echo "NAME: ${NAME}"
				echo "TEXT: ${TEXT}"
				echo "TOGGLE: ${TOGGLE}"
				echo "CHOICE: ${CHOICE}"
				echo "PASSWORD: ${PASSWORD}"
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
