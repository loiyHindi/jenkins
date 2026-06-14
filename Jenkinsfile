pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Run Node App') {
            steps {
                sh 'node index.js'
            }
        }
    }

    post {
        success {
            echo 'Build SUCCESS ✔'
        }

        failure {
            echo 'Build FAILED ✖'
        }
    }
}