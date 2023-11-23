pipeline {
                         agent {
                         docker {
                           image 'python:3.7'
                           reuseNode true
                         }
                       }
  stages {
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
