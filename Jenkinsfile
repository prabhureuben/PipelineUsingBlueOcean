pipeline {
  agent any
  stages {
    stage('Development Build') {
      steps {
        echo 'Pull the code from Git Hub Repository'
        echo 'Create a Build Using Repository'
      }
    }

    stage('Smoke Test') {
      steps {
        echo 'Run Two Smoke Test'
      }
    }

    stage('Deploy in QA Environment') {
      steps {
        echo 'Stop the Server'
        echo 'Move the build in QA'
        echo 'Start the server'
        echo 'Notify to QA by Email'
      }
    }

    stage('Integration Test') {
      parallel {
        stage('Integration Test') {
          steps {
            echo 'UI Based Testing'
          }
        }

        stage('API Testing') {
          steps {
            echo 'Run Rest Automation Tests'
          }
        }

        stage('Performance Testing') {
          steps {
            echo 'Run Jmeter Tests'
          }
        }

      }
    }

    stage('Certify') {
      steps {
        echo 'QA Team Certify'
      }
    }

  }
}