pipeline {
  agent any
  tools {
    maven 'mvn'
  }
  stages {
    stage('build') {
      steps {
        sh 'sudo apt update'
        sh 'sudo apt install -y maven'
        sh 'mvn clean install'
        sh 'mvn package'
      }
    }

  }
}