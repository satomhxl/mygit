pipeline {
  agent {
    node {
      label 'huashan'
    }

  }
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