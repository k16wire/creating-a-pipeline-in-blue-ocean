pipeline {
  agent {
    docker {
      image 'node:6-alpine'
    }

  }
  stages {
    stage('build') {
      steps {
        sh '''npm install
'''
      }
    }
    stage('test') {
      steps {
        sh './jenkins/scripts/test.sh'
      }
    }
    stage('deploy') {
      steps {
        sh './jenkins/scripts/deliver.sh'
      }
    }
  }
}