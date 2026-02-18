pipeline {
  agent { label: 'linux' }

  options {
    skipDefaultCheckout(true)
  }

  stages {
    stage('Checkout') {
      steps {
        deleteDir()
        checkout scm
      }
    }
    
    stage('Run Script') {
      steps {
        sh 'chmod +x hello.sh && ./hello.sh'
        sh 'ls -la'
      }
    }
  }
}
