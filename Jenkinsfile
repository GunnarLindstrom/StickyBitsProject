pipeline {
	agent any
	
	stages {

		stage('Clean-up') {
                        steps {
                                dir("Docker/") {
                                        sh './clean_up_docker.sh'
                                }
                        }
		}

		stage('Deploy') {
			steps {
				dir("Docker/") {
					sh 'docker-compose up --build -d'
				}		
			}
		}
	}
}

