pipeline {
  agent any
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