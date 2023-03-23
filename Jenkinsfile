pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          agent any
          steps {
            echo 'Building...'
          }
        }

        stage('Test') {
          agent any
          steps {
            echo 'Testing...'
          }
        }

        stage('Deploy') {
          agent any
          steps {
            echo 'Deploying...'
          }
        }

      }
    }

    stage('Waiting') {
      agent any
      steps {
        input(message: 'Proceed?', id: 'Proceed')
      }
    }

  }
}