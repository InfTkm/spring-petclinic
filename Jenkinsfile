pipeline {
  agent any
  tools {
    maven 'mvn'
  }
  stages {
    stage('build') {
      steps {
        sh 'rm -rf ~/.m2/repository'
        sh './mvnw clean install'
        sh './mvnw package'
      }
    }

  }
}