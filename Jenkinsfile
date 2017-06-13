pipeline {
  agent any
  stages {
    stage('Make Bake') {
      steps {
        echo 'Building..'
        sh '''cd build
                #make
                #java build
                #rm -f build.jar build.class
                echo "building some major stuff right here...." '''
      }
    }
    stage('Make Test 1') {
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
    stage('Make Test 2') {
      steps {
        echo 'System testing'
      }
    }
    stage('Make Deploy') {
      steps {
        echo 'Deploying....'
        sleep 5
      }
    }
  }
}




