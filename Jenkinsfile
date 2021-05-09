pipeline {
  agent any
  stages {
    stage('SCM') {
      steps {
        git(url: 'https://github.com/coirne/PROJET_FINAL.git', branch: 'main')
      }
    }

    stage('docker') {
      steps {
        dockerNode(image: 'node:14-alpine') {
          sh 'node --version'
        }

      }
    }

  }
}