pipeline {
  agent none
  stages {
    stage('shell') {
      parallel {
        stage('shell') {
          steps {
            sh 'echo "I am first job"'
          }
        }
        stage('build') {
          steps {
            sleep 5
          }
        }
      }
    }
    stage('execute') {
      steps {
        git(url: 'git@github.com:pratik78/testrepo.git', branch: 'master')
      }
    }
  }
}