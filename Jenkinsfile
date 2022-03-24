pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'Build Stage'
          }
        }

        stage('') {
          steps {
            bat(script: 'echo \'hello to build\'', returnStatus: true, returnStdout: true)
          }
        }

      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'test stage'
          }
        }

        stage('') {
          steps {
            dir(path: 'test')
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'Deploy stage'
      }
    }

  }
  environment {
    Key = 'Value'
  }
}