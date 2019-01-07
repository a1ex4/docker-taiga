pipeline {
  agent any
  stages {
    stage('Update') {
      steps {
        sh 'git submodule update --remote'
      }
    }
  }
}