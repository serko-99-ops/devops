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
        stage('log') {
          steps {
            sh 'cd curriculum-front && npm i && npm run  test:unit'
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