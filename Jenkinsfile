pipeline {
  agent any
  stages {
    stage('1st') {
      steps {
        tool(name: 'nodejs', type: 'nodejs')
        git(url: 'https://github.com/jcavaiuolo/nodejs-helloworld-api.git', branch: 'main')
      }
    }

    stage('2nd') {
      steps {
        tool(name: 'nodejs', type: 'nodejs')
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