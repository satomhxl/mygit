pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'gcc test.c'
      }
    }

    stage('run') {
      steps {
        sh './a.out'
      }
    }

  }
}