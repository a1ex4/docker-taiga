pipeline {
  agent any
  stages {
    stage('Update') {
      steps {
        sh 'git submodule update --remote'
        sh 'git submodule foreach git pull origin master'
        sh 'git pull'
        sh 'ls -l'
        sh 'git submodule init'
        sh 'git submodule update'
      }
    }
    stage('Build image') {
      steps {
        sh 'docker build -t a1ex4/rpi-taiga .'
      }
    }
  }
}