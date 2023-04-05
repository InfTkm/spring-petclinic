pipeline {
  agent any
  tools {
    maven 'mvn'
  }
  stages {
    stage('build') {
      steps {
        sh 'apt update'
        sh 'apt install -y maven'
        sh 'mvn clean install'
        sh 'mvn package'
      }
    }

  }
}