pipeline {
  agent {
    docker {
      args '-p 8989:8989'
      image 'node:6-alpine'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }

    stage('Test') {
      environment {
        CI = 'true'
      }
      steps {
        sh './jenkins/scripts/test.sh'
      }
    }

  }
}