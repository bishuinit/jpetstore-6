pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'First Jenkins Pipeline'
        sh './mvnw clean compile'
      }
    }

    stage('Unit Test') {
      steps {
        sh '''./mvnw test
'''
        junit '**/target/surefire-reports/TEST-*.xml'
      }
    }

  }
}