pipeline {
  agent {
    docker {
      image 'maven:latest'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        git(url: 'ssh://jenkins@gerrit:29418/MDC/DEMO/demo-base-spring-petclinic', branch: 'master', credentialsId: 'adop-jenkins-master', poll: true)
      }
    }
  }
  environment {
    WORKSPACE_NAME = 'MDC'
    PROJECT_NAME = 'MDC/DEMO'
  }
}