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
        sh ' npm install'
      }
    }

    stage('Test') {
      steps {
        echo 'It is test'
        sh './jenkins/scripts/test.sh'
      }
    }

    stage('Delivery') {
      steps {
        echo 'It is Delivery'
        sh './jenkins/scripts/deliver.sh'
        echo 'Finished using the web site? (Click "Proceed" to continue'
        sh './jenkins/scripts/kill.sh'
      }
    }

  }
}