pipeline {
  agent { 
      docker { 
        image 'python:3.7.3' 
      }
  }
  stages {
    stage('build') {
      steps {
        sh 'whoami; pwd; ls -al'
      }
    }
    stage('test') {
      steps {
        sh 'source .venv/bin/activate; pytest tests'
      }   
    }
  }
}
