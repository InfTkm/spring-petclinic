pipeline {
  agent any

  stages {
    stage('build') {
      steps {
        sh 'java -version'
        sh './mvnw install'
        sh './mvnw package'
        sh 'cp target/*.jar /var/tmp'
      }
    }

    stage('deploy') {
      steps {
        sh 'ansible-playbook deploy_petclinic.yml'
      }
    }

  }
}