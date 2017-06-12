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
                echo "building some major stuff right here...." '''
            }
        }

        stage('Testing Phase 1') {
            steps {
                parallel test1: {
                    echo 'unit testing'
                },
                test2: {
                    echo 'integration testing'
                }
            }
        }
       stage('Testing Phase 2') {
           steps {
               echo 'System testing'
           }
       }
       stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
      }
   }
}
