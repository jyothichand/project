pipeline {
    agent any

    stages {
        stage('validate') {
            steps {
                echo 'validating..'
		sh 'pwd'
		sh 'mvn compile'
            }
        }
        stage('unit testing') {
            steps {
                echo 'Testing..'
		sh 'pwd'
		sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
	
            }
        }
    }
}

