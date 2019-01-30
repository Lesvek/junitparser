pipeline {
  agent any
  stages {
    stage('Unittests') {
      parallel {
        stage('Unittests') {
          steps {
            sh 'python -m pytest'
          }
        }
        stage('lint') {
          steps {
            sh 'flake8'
          }
        }
      }
    }
  }
}