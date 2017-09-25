pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo \'Hello World\''
        git(url: 'https://github.com/OscarDHdz/bo-test-2/blob/master/Jenkinsfile', branch: '*/master')
      }
    }
  }
}