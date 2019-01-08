pipeline {
  agent any
  stages {
    stage('Update') {
      steps {
        sh 'ls -l'
        sh 'git submodule init'
        sh 'git submodule update'
        sh 'git submodule update --remote'
        sh 'git submodule foreach git pull origin master'
        sh 'git pull'
      }
    }
    stage('Build image') {
      steps {
        sh 'docker build -t a1ex4/rpi-taiga .'
      }
    }
  }
}