pipeline {
  agent {
    docker {
      image 'node:20.9.0-alpine3.18'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Build') {
      steps {
        echo 'It is build'
        sh 'sh \'npm install\''
      }
    }

    stage('Test') {
      steps {
        echo 'It is test'
      }
    }

    stage('Delivery') {
      steps {
        echo 'It is Delivery'
      }
    }

  }
}