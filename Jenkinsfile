pipeline {
  agent any
  stages {
    stage('Checkout code') {
      steps {
        git(url: 'https://github.com/rohan0246/sample-code', branch: 'main')
      }
    }

    stage('log') {
      parallel {
        stage('log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('front-unit test') {
          steps {
            sh 'cd curriculum-front && npm i && npm  run test:unit'
          }
        }

      }
    }

  }
}