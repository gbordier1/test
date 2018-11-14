pipeline {
    agent any

    stages {
        stage('Checkout scm') {
            steps {
                echo 'Checkout..'
		cleanWs()
		checkout scm
            }
        }
        stage('Package') {
            steps {
                echo 'Package..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}

