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
        sh 'env'
        sh 'echo $PATH'
        sh "sshpass -p '123456' scp -o StrictHostKeyChecking=no /var/tmp/spring-petclinic-3.0.0-SNAPSHOT.jar root@petclinic:/app/"
        sh 'ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -i inventory.ini deploy_petclinic.yml'
      }
    }
  }
}