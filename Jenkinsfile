pipeline {
  agent any
  tools {
    maven 'mvn'
  }
  stages {
    stage('build') {
      steps {
        sh './mvnw clean install'
        sh './mvnw package'
      }
    }

  }
}