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
//          stage('Init') { 
  //          steps {
    //            sh 'npm init -y'
      //      }
        //  }
          stage('Build') {
            steps {
            sh 'pwd'
            sh 'du -a'
                sh 'npm install'
            }
          }
          stage('Test') { 
            steps {
                sh './jenkins/scripts/deliver.sh' 
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
