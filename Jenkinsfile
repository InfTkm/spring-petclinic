pipeline {
  agent any
  tools {
    maven 'mvn'
  }
  environment {
    JAVA_HOME='/home/unx/.jdks/corretto-16.0.2'
    PATH="${JAVA_HOME}/bin:${env.PATH}"
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