pipeline {
  agent any

  stages {
    stage('build') {
      steps {
        sh 'java -version'
        sh './mvnw clean install'
        sh './mvnw package'
      }
    }

  }
}