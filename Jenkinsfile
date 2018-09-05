pipeline {
  agent any
  stages {
    stage('Say Hello') {
      steps {
        echo 'Hello World!'
        sh 'java -version'
        echo "${MY_NAME}"
      }
    }
    stage('Deploy') {
      options {
        timeout(time: 30, unit: 'SECONDS')
      }
      input {
        message 'Should we continue?'
      }
      steps {
        echo 'Continuing with deployment'
        input(message: 'Ci fermiamo o andiamo avanti?', id: '1', ok: '2')
      }
    }
  }
  environment {
    MY_NAME = 'Paola'
  }
}