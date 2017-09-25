pipeline {
  agent any
  stages {
    stage('Initialize') {
      steps {
        git(url: 'ssh://jenkins@gerrit:29418/MDC/DEMO/demo-base-spring-petclinic', credentialsId: 'adop-jenkins-master', branch: 'master')
      }
    }
  }
  environment {
    WORKSPACE_NAME = 'MDC'
    PROJECT_NAME = 'MDC/DEMO'
  }
}