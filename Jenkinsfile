pipeline {
  agent any
  stages {
    stage('Initialize') {
      steps {
        git(url: 'ssh://jenkins@gerrit:29418/MDC/DEMO/demo-base-spring-petclinic', credentialsId: 'adop-jenkins-master', branch: 'master')
        node(label: 'java8') {
          echo '-123'
          sh 'mvn clean install'
        }
        
        echo 'Hola'
      }
    }
  }
  environment {
    WORKSPACE_NAME = 'MDC'
    PROJECT_NAME = 'MDC/DEMO'
  }
}