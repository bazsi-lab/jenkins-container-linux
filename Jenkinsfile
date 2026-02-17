pipeline {
  agent { label 'container-linux' }

  stages {
    stage('Hello') {
      steps {
        echo "Hello from ${env.NODE_NAME}"
      }
    }
  }
}
