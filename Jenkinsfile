pipeline {
  agent any
  stages {
    stage('Deploy') {
      steps {
        echo 'Deploying...'
        sh 'python3 app.py'
        // e.g. push image or run deploy scripts
      }
    }
  }
}
