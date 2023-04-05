pipeline {
  agent {
    docker {
      image 'openjdk:16-jdk'
    }
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