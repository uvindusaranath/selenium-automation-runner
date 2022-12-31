pipeline{
	agent any
	stages{
		stage("Start Grid"){
			steps{
				sh "docker-compose up"
			}
		}
		stage("Run Test"){
			steps{
				sh "docker-compose up search-module book-flight-module"
			}
		}
	}
	post{
		always{
			sh "docker-compose down"
		}
	}
}
