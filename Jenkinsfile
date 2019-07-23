pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Install Gems') {
			steps {
				 sh "./deploy"
			}
        }		
        stage('Test') {
            steps {
                sh 'bundle install'
            }
        }
        stage('Deploy') {
            steps {
                rspec spec
            }
        }
    }
}
