pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
		            echo 'Building..'
                sh '''cd build
                make
                java Build
                #rm -f build.jar build.class
                '''
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
	stage('Blar') {
	   steps {
		echo ' balr ......'
	   }
	}
    }
}
