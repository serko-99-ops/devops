pipeline {
  agent any
  stages {
    stage('checkout code') {
      steps {
        git(branch: 'dev', url: 'https://github.com/faraday-academy/curriculum-app')
      }
    }

  }
}