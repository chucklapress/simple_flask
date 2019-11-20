pipeline {
  agent { docker { image 'python:2.7.17' } }
  stages {
    stage('build') {
      steps {
        sh 'pip install -r requirements.txt'
      }
    }
    stage('set') {
      steps {
        sh 'python app.py'
      }
    }
    stage('test') {
      steps {
        sh 'python test.py'
      }
    }
  }
}
