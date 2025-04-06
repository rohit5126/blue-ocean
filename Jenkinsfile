pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''pwd
date'''
        echo '$name and $age'
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            sleep(unit: 'SECONDS', time: 10)
          }
        }

        stage('test1') {
          steps {
            sh 'ls -lh'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploy the app'
      }
    }

  }
  environment {
    name = 'rohit'
    age = '23'
  }
}