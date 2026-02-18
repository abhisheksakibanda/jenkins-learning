pipeline {
    agent any

    options {
        skipDefaultCheckout(true)
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
                sh 'ls -la'
            }
        }

        stage('Run Script') {
            steps {
                sh 'chmod +x hello.sh'
                sh './hello.sh'
            }
        }

        stage('Create Local File') {
            steps {
                sh 'echo "I am not tracked by git" > local.txt'
                sh 'ls -la'
            }
        }
    }
}
