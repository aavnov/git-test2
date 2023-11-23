pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000'
        }
    }
    environment {
        CI = 'true' 
    }
  stages {
          stage('Build') {
            steps {
                sh 'npm install'
            }
          }
          stage('Test') { 
            steps {
                sh './jenkins/scripts/test.sh' 
            }
        }
          stage('One') {
            steps {
              echo 'Hi, this is Zulaikha from edureka'
            }
          }
          stage('Two') {
            steps {
              input('Do you want to proceed?')
            }
          }
          stage('Three') {
            when {
                not {
                     branch "master"
                }
            }
            steps {
                echo "Hello"
            }
          }
          stage('Four') {
            parallel { 
                    stage('Unit Test') {
                      steps {
                         echo "Running the unit test..."
                      }
                    }
                    stage('Integration test') {

                       steps {
                         echo "Running the integration test..."
                       }
                    }
            }
          }
 
  }
}
