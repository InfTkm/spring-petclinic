pipeline {
  agent any
  tools {
    maven 'mvn'
  }
  stages {
    stage('build') {
      steps {
        sh 'mvn clean install'
        sh 'mvn package'
      }
    }

  }
}