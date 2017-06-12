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

          parallel Test1: {
          echo 'test1'


      }, Test2: {
          echo 'test2'
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
