pipeline {
  agent any
  environment {
    ANSIBLE_HOST_KEY_CHECKING = 'False'
    ANSIBLE_PRIVATE_KEY_FILE = '/var/lib/jenkins/.ssh/ansible_key'
  }
  stages {
    stage('Deploy Docker Image on Master') {
      steps {
        // Ansible Playbook을 실행하여 Docker 이미지를 배포합니다.
        sh 'ansible-playbook -i /etc/ansible/hosts playbook.yml'
      }
    }
  }
}

