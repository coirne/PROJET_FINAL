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
        dockerNode(image: 'ahmed24khaled/ansible-management') {
          sh 'ansible-playbook -v -i ./ansible_provisinning/hosts ./ansible_provisinning/playbook.yml'
        }

      }
    }

  }
}