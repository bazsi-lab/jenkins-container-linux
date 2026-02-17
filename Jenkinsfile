pipeline {
  agent { label 'container-linux' }

  stages {
    stage('Hello') {
      steps {
        echo "Hello from Bello ${env.NODE_NAME}"
      }
    }
  }
}
