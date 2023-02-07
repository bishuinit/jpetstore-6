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

    stage('Static Analysis') {
      steps {
        sh '''./mvnw sonar:sonar \\
  -Dsonar.host.url=http://172.31.89.246:9000/ \\
  -Dsonar.projectKey=JPetstore \\
  -Dsonar.login=sqp_f89a2a891407be1f68c358a74668a61a842ba627'''
      }
    }

  }
}