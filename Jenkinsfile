pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building...'
          }
        }

        stage('Test') {
          steps {
            echo 'Testing...'
          }
        }

        stage('Deploy') {
          steps {
            echo 'Deploying...'
          }
        }

      }
    }

    stage('Waiting') {
      steps {
        input(message: 'Proceed?', id: 'Proceed')
      }
    }

  }
}