pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "${params}"
                echo "Targets: ${params.TARGETS}"
                echo 'Building..'
                sh "make ${params.TARGETS}"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'docker images'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}