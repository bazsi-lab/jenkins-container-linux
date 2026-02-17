pipeline {
  agent any

  tools {
    maven 'maven-3.9.12'
  }

  stages {

    stage('Hello') {
      steps {
        echo 'HELLO FROM JENKINS'
      }
    }

    stage('Maven Version') {
      steps {
        sh 'mvn -version'
      }
    }

    stage('Test') {
      steps {
        sh 'mvn -B test'
      }
      post {
        always {
          junit testResults: '**/target/surefire-reports/TEST-*.xml',
                allowEmptyResults: false
        }
      }
    }

    stage('Package') {
      steps {
        sh 'mvn -B package'
      }
    }
  }
}
