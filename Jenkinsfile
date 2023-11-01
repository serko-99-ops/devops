pipeline {
  agent any
  stages {
    stage('checkout code') {
      steps {
        git(branch: 'dev', url: 'https://github.com/faraday-academy/curriculum-app')
      }
    }

    stage('error') {
      parallel {
        stage('error') {
          steps {
            sh 'ls -la'
          }
        }

        stage('front-end') {
          steps {
            sh 'cd curriculum-front && npm i && npm test:unit'
          }
        }

      }
    }

  }
}