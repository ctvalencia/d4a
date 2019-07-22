pipeline {
	agent any
	stages{
		stage('Initial setup'){
			steps{
				sh 'echo starting'
			}
		}
		stage('Checking Docker'){
			steps{
				sh 'sudo docker ps'
			}
		}
		stage('Build Docker'){
			steps{
				sh 'sudo docker-compose down'
				sh 'sudo docker build --tag=php54 .'
				sh 'sudo docker run -p 80:80 --rm -d --name=php54 php54'
				sh 'pwd'
				sh 'ls'
			}
		}
	}
}
