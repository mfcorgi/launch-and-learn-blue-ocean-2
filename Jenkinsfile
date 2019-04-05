pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'message 2'
        echo 'Build done!'
      }
    }
    stage('Testing') {
      steps {
        input 'Are you ready for testing?'
      }
    }
    stage('Integration Test') {
      parallel {
        stage('Integration Test') {
          steps {
            echo 'Integration Test done!'
          }
        }
        stage('Unit Tests') {
          steps {
            echo 'Unit Tests Done!'
          }
        }
        stage('Smoke Test') {
          steps {
            echo 'Smoke Tests done!'
          }
        }
      }
    }
    stage('Testing Ready') {
      steps {
        echo 'Are you ready to deploy?'
        input 'Are you ready to deploy?'
      }
    }
    stage('Deploy') {
      steps {
        echo 'deploy done!'
      }
    }
  }
}