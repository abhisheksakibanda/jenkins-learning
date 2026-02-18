pipeline {
  agent { label 'controller' }

  stages {
    stage('Docker Sanity') {
      steps {
        sh 'docker version'
        sh 'docker ps'
      }
    }
    
    stage('Run inside Container') {
      steps {
        script {
          docker.image('python:3.12-slim').inside {
            sh 'python3 --version'
            sh 'python -c "print(\'Hello from inside the Docker Container\')"'
          }
        }
      }
    }
  }
}
