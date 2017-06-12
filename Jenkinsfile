pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
		            echo 'Building..'
                sh '''cd build
                #make
                #java build
                #rm -f build.jar build.class
                echo 'building some major stuff right here....'
                '''
            }
        }

        stage('Test'){
          parallel (
            "JUnit": {
                echo "echo JUnit"
                },

            "DBUnit": {
                sh "echo DBUnit"
                },
            "Jasmine": {
                sh "echo Jasmine"
              },
              )
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


stage('Test'){
      parallel (
        "JUnit": {
            sh "echo JUnit"
        },
        "DBUnit": {
            sh "echo DBUnit"
        },
        "Jasmine": {
            sh "echo Jasmine"
        },
      )
