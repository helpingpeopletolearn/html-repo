pipeline {
  agent any
  stages {
    stage('Fetch code') {
      steps {
        git(url: 'git@github.com:helpingpeopletolearn/html-repo.git', branch: 'main', poll: true)
      }
    }

    stage('Install apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('Deploy app') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}