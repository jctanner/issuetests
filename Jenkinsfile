pipeline {
  agent { 
      docker { 
        image 'python:3.7.3' 
      }
  }
  stages {
    stage('build') {
      steps {
        sh 'apt-get update; apt-get install python-virtualenv; virtualenv --python=/usr/local/bin/python3; .venv; source .venv/bin/activate; pip install -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        sh 'source .venv/bin/activate; pytest tests'
      }   
    }
  }
}
