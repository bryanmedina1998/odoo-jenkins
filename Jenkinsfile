pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Hola mundo'
      }
    }

    stage('Ping') {
      steps {
        sh 'ansible all -i hosts -m ping -f 5'
      }
    }

    stage('Install Docker') {
      steps {
        sh '''- hosts: all
  become: yes
  tasks:
   - name: install Docker
     apt:
       name: docker.io
       state: present
       update_cache: true
       
   - name: install Docker-compose
     apt:
       name: docker-compose
       state: present
       update_cache: true'''
      }
    }

  }
}