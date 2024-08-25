pipeline {
  agent any
  stages {
    stage('1st') {
      steps {
        git(url: 'https://github.com/jcavaiuolo/nodejs-helloworld-api.git', branch: 'main')
      }
    }

    stage('2nd') {
      steps {
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        sh 'npm test'
      }
    }

    stage('Start') {
      steps {
        sh 'npm start'
      }
    }

  }
}