pipeline {
  agent any
  stages {
    stage('nodejsTool') {
      steps {
        tool(name: 'nodejs', type: 'nodejs')
      }
    }

    stage('gitClone') {
      steps {
        git(url: 'https://github.com/jcavaiuolo/nodejs-helloworld-api.git', branch: 'main')
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

    stage('npmBuild') {
      steps {
        sh 'npm build'
      }
    }

    stage('curl') {
      steps {
        sh 'curl http://localhost:3000'
      }
    }

  }
}