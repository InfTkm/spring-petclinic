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
        sh 'ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -i inventory.ini deploy_petclinic.yml'
      }
    }

  }
}