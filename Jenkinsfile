pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Hola mundo'
      }
    }

    stage('Building') {
      steps {
        sh 'ansible all -i hosts -m ping -f 5'
      }
    }

  }
}