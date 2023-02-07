pipeline {
  agent {
    node {
      label 'test'
    }

  }
  stages {
    stage('Build') {
      steps {
        echo 'First Jenkins Pipeline'
        sh '/mvnw clean compile'
      }
    }

  }
}