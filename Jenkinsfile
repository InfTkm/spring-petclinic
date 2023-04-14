pipeline {
  agent any

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
        sh 'ansible-playbook -i deploy_petclinic.yml'
      }
    }

  }
}