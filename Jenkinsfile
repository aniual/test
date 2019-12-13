pipeline {
  agent any
  stages {
    stage('fetch') {
      steps {
        git(url: 'git@github.com:aniual/test.git', branch: 'master')
      }
    }

  }
}