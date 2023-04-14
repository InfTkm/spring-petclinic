pipeline {
  agent any

  stages {
    stage('build') {
      steps {
        sh './mvnw install'
        sh './mvnw package'
        sh 'cp target/*.jar /var/tmp'
      }
    }

    stage('deploy') {
      steps {
        sh "sshpass -p '123456' scp /var/tmp/spring-petclinic-3.0.0-SNAPSHOT.jar root@localhost:/app/"
        sh 'ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -i inventory.ini deploy_petclinic.yml'
      }
    }
  }
}