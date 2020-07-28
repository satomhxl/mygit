pipeline {
  agent {
    node {
      label 'huashan'
    }

  }
  stages {
    stage('build') {
      steps {
        sh '''pwd
ls
gcc test.c'''
      }
    }

    stage('run') {
      steps {
        sh '''pwd
ls
./a.out'''
      }
    }

  }
}