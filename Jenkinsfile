pipeline {
  agent any
  stages {
    stage('Build Image') {
      steps {
        sh 'docker build -t cicd-devops .'
      }
    }
    stage('Run Container') {
      steps {
        sh 'docker run -d -p 5001:5000 cicd-devops || true'
      }
    }
  }
}
