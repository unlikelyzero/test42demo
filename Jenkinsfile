pipeline {
  agent any
  stages {
    stage('NPM Build') {
      steps {
        sleep 3
      }
    }
    stage('Unit Tests') {
      steps {
        sleep 5
      }
    }
    stage('UI Testing') {
      parallel {
        stage('UI Testing') {
          steps {
            echo 'I\'m Testing with Selenium'
          }
        }
        stage('Chrome') {
          steps {
            sleep 3
          }
        }
        stage('Ffox') {
          steps {
            sleep 5
          }
        }
        stage('IE11') {
          steps {
            sleep 7
            sh 'exit 1'
          }
        }
      }
    }
    stage('Reporting') {
      steps {
        sleep 1
      }
    }
    stage('Staged in Productino') {
      steps {
        sleep 1
      }
    }
  }
}