pipeline {
  agent any
  stages {
    stage('Update') {
      steps {
        sh 'ls -l'
        sh 'git submodule init'
        sh 'git submodule update'
        sh 'git submodule update --remote'
      }
    }
    stage('Build image') {
      steps {
        sh 'docker build -t a1ex4/rpi-taiga .'
      }
    }
  }
}