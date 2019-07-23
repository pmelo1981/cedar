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
        stage('Bundle Install') {
            steps {
                sh 'bundle install'
            }
        }
        stage('RSPEC TESTING') {
            steps {
                sh 'rspec spec'
            }
        }
    }
}
