pipeline {
  agent any
  stages {
    stage('make bake') {
      steps {
        echo 'Building..'
        sh '''cd build
                #make
                #java build
                #rm -f build.jar build.class
                echo "building some major stuff right here...." '''
      }
    }
    stage('make test') {
      steps {
        parallel(
          "unit": {
            echo 'unit testing'
            
          },
          "integration": {
            echo 'integration testing'
            sleep 10
            
          }
        )
      }
    }
    stage('make deploy') {
      steps {
        echo 'Deploying....'
        sleep 5
      }
    }
  }
}




