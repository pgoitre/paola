pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        git 'https://github.com/pgoitre/paola/blob/master/helloworld'
      }
    }
    stage('SonarQube analysis 1') {
      steps {
        sh 'mvn clean package sonar:sonar'
      }
    }
  }
}