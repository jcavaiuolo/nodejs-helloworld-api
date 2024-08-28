pipeline {
  agent {
    node {
      label 'nodejs'
    }

  }
  stages {
    stage('CloneRepo') {
      steps {
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

  }
}