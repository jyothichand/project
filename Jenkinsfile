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
        stage('build') {
            steps {
                echo 'building....'
		sh 'pwd'
		sh 'mvn clean package'
	
            }
        }
	stage('sonar-test') {
            steps {
                echo "performiong sonar analysis"'
		sh 'pwd'
		sh 'mvn sonar:sonar \
  -Dsonar.host.url=http://3.215.133.23:9000 \
  -Dsonar.login=c06b5984bea0fa6180065bce325b1b376611ecf5

            }
        }
    }
}

