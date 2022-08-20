pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        sh 'ls -lha /'
      }
    }

    stage('Formatting and Validation') {
      steps {
        sh 'ls -lha'
      }
    }

    stage('Generate Builds and Tests') {
      steps {
        sh 'ls'
      }
    }

    stage('Windows Build') {
      parallel {
        stage('Windows Build') {
          steps {
            sh 'ls'
          }
        }

        stage('MacOS Build') {
          steps {
            sh 'ls'
          }
        }

        stage('Linux Build') {
          steps {
            echo 'ok'
          }
        }

      }
    }

    stage('Windows Test') {
      parallel {
        stage('Windows Test') {
          steps {
            sh 'ls'
          }
        }

        stage('MacOS Test') {
          steps {
            sh 'ls'
          }
        }

        stage('Linux Test') {
          steps {
            sh 'ls'
          }
        }

      }
    }

    stage('Finalize') {
      steps {
        sh 'ls'
      }
    }

  }
}