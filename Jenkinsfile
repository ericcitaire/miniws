pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Compile') {
          steps {
            echo 'Compiling...'
            sleep 5
          }
        }
        stage('Code Quality') {
          steps {
            echo 'Code Quality...'
            sleep 2
          }
        }
      }
    }
    stage('Deploy to QA') {
      steps {
        echo 'Deploying to QA...'
        sleep 8
      }
    }
    stage('Tests') {
      parallel {
        stage('UI Tests') {
          steps {
            echo 'Testing UI...'
            sleep 7
          }
        }
        stage('Performance Tests') {
          steps {
            echo 'Testing Performances...'
            sleep 10
          }
        }
        stage('Security Tests') {
          steps {
            echo 'Testing Security...'
            sleep 2
          }
        }
      }
    }
    stage('Deploy to Prod') {
      steps {
        echo 'Deploying to Prod...'
        sleep 5
      }
    }
  }
}