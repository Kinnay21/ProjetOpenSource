pipeline {
  agent none
  stages {
    stage('test') {
      steps {
        echo 'test script'
      }
    }

    stage('test2') {
      parallel {
        stage('test2') {
          steps {
            sh 'echo \'hello1\''
            sh 'echo \'hello2\''
          }
        }

        stage('test3') {
          steps {
            sh 'echo hello3'
          }
        }

      }
    }

    stage('stage end') {
      steps {
        sh 'echo \'good bye\''
      }
    }

  }
}