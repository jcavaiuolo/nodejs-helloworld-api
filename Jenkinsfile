pipeline {
  agent any
  stages {
    stage('CloneRepo') {
      steps {
        tool(name: 'nodejs', type: 'nodejs')
        sh 'git clone https://github.com/jcavaiuolo/nodejs-helloworld-api.git'
      }
    }

    stage('npmInstall') {
      steps {
        sh 'npm install'
      }
    }

    stage('npmTest') {
      steps {
        sh 'npm test'
      }
    }

    stage('npmStart') {
      steps {
        sh 'npm start'
      }
    }

    stage('curl') {
      steps {
        sh 'curl http://localhost:3000'
      }
    }

  }
}