pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh './mvnw clean install'
        sh './gradlew build'
      }
    }

  }
}