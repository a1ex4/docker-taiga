pipeline {
  agent any
  stages {
    stage('Update') {
      steps {
        sh 'git submodule update --remote'
        sh 'git submodule foreach git pull origin master'
        sh 'git pull'
        sh 'ls -l'
      }
    }
  }
}