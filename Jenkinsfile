pipeline {
  agent any
  stages {
    stage('SCM') {
      steps {
        git 'https://github.com/pgoitre/paola'
      }
    }
    stage('build && SonarQube analysis') {
      steps {
        withSonarQubeEnv('Sonar') {
          withMaven(maven: 'Maven 3.5') {
            sh 'mvn clean package sonar:sonar'
          }

        }

      }
    }
  }
}