pipeline {
  agent any

  tools {
    maven 'maven-3.9.12'
  }

  stages {

    stage('Hello') {
      steps {
        echo 'HELLO FROM JENKINS PIPELINE 🚀'
        sh 'echo HELLO FROM SHELL'
      }
    }

    stage('Build') {
      steps {
        sh 'mvn -version'
      }
    }
  }
}
