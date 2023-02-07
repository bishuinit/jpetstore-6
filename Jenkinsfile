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
  -Dsonar.projectKey=JPStore2 \\
  -Dsonar.login=sqp_c7804c710ac0466f180bbc1fc8113c1ab1fa3995'''
      }
    }

  }
}