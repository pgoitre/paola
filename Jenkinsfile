pipeline {
  agent any
  stages {
    stage('Example') {
      steps {
        writeFile(file: 'myFile.txt', text: libraryResource("path/to/myFile.txt"))
      }
    }
  }
}