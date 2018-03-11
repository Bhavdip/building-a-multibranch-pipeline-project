pipeline {
  agent {
    docker {
      image 'node:6-alpine'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        echo 'Hello Build'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy Message'
      }
    }
  }
}