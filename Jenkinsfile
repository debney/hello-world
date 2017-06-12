pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
		            echo 'Building..'
                sh '''cd build
                pwd
                make
                java build
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
