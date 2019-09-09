pipeline {
  agent { docker { image 'python:3.7.3' } }
  stages {
    stage('build') {
      steps {
        sh 'whoami; pip install -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        sh 'pytest tests'
      }   
    }
  }
}
