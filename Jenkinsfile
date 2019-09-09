pipeline {
  agent { 
      docker { 
        image 'python:3.7.3' 
      }
  }
  stages {
    stage('build') {
      steps {
        sh 'virtualenv .venv; source .venv/bin/activate; pip install -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        sh 'source .venv/bin/activate; pytest tests'
      }   
    }
  }
}
