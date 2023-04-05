pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh './mvnw clean install'
        sh './mvnw package'
      }
    }

  }
}