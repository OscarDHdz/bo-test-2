pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'http://54.89.141.195/gerrit/MDC/DEMO/demo-base-spring-petclinic', branch: '*/master', credentialsId: 'adop-jenkins-master')
        sh 'echo \'Hello World\''
      }
    }
  }
}