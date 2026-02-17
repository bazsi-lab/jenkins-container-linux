pipeline {
    agent any

    tools {
        maven 'maven-3.9.12'
    }

    stages {

        stage('Build') {
            steps {
                sh 'mvn -version'
                sh 'mvn -B -DskipTests package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn -B test'
            }
            post {
                always {
                    junit '**/target/surefire-reports/TEST-*.xml'
                }
            }
        }
    }
}
