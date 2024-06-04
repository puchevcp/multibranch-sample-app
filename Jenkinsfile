pipeline {
  agent {label 'windows'}
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  stages {
    stage('hello') {
      steps {
        echo "hello"
      }
    }
    stage('cat README') {
     when {
       branch "fix-*"
     }
     steps {
      sh '''
        cat README.md
      '''
     }
    }
  }
}
