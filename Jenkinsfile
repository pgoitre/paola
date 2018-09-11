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
          sh '/opt/maven/bin/mvn clean package sonar:sonar'
        }

      }
    }
  }
}