pipeline {
  agent {
    node {
      label 'huashan'
    }

  }
  triggers { pollSCM('H/1 * * * *') }
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            sh '''pwd
ls
gcc test.c'''
          }
        }

        stage('clone another repository') {
          steps {
            sh '''rm -rf subDir
mkdir subDir'''
            dir(path: 'subDir') {
              sh '''pwd
ls'''
              git(url: 'https://github.com/satomhxl/jenkinsTest.git', branch: 'master', credentialsId: 'github-id')
              sh '''pwd
ls
gcc test.c'''
            }

            sh '''pwd
ls
gcc test.c'''
          }
        }

      }
    }

    stage('run') {
      parallel {
        stage('run') {
          steps {
            sh '''pwd
ls
./a.out'''
          }
        }

        stage('run another repository') {
          steps {
            dir(path: 'subDir') {
              sh '''pwd
ls
./a.out'''
            }

          }
        }

      }
    }

  }
}
