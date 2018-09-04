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
  }
  environment {
    MY_NAME = 'Paola'
  }
}