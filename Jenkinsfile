pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker-compose build'
        sh 'docker-compose up -d'
      }
    }
    stage('Test') {
      steps {
        sh 'docker-compose exec app python -m pytest || true'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying...'
        // e.g. push image or run deploy scripts
      }
    }
  }
  post {
    always {
      sh 'docker-compose down'
    }
  }
}
