pipeline {
  agent any
  stages {
    stage('Clone Repo') {
      steps {
        git 'https://github.commatin0143/flask-app.git'
      }
    }
    stage('Install Dependencies') {
      steps {
        sh 'pip3 install -r requirements.txt'
      }
    }
    stage('Restart App') {
      steps {
        sh 'pm2 restart flask-app || pm2 start app.py --interpreter python3 --name flask-app'
      }
    }
  }
}
