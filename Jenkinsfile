pipeline {
    agent any

    stages {
        stage('Build') {
            steps {

		sh '''#!/bin/bash
		DOCKER_LOGIN=`aws ecr get-login --region eu-west-1`
		${DOCKER_LOGIN}'''               

 
		echo 'Building..'
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
    }
}
