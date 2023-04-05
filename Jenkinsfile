pipeline {
  agent any

  tools {
    jdk 'java17'
  }

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