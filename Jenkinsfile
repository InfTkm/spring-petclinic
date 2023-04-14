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
        sh 'co target/*.jar /var/tmp'
      }
    }

    stage('deploy') {
      steps {
        sh 'ansible-playbook -i inventory.ini deploy_petclinic.yml'
      }
    }

  }
}