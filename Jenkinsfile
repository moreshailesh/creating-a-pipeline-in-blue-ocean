pipeline {
  agent {
    docker {
      image 'node:10-alpine'
      args '-p 8989:8989'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }

  }
}