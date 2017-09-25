pipeline {
  agent {
    node {
      label 'java8'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        sh '''echo \'Hello World\'
echo $PROJECT_NAME'''
        git(url: 'ssh://jenkins@gerrit:29418/MDC/DEMO/demo-base-spring-petclinic', branch: 'master', credentialsId: 'adop-jenkins-master', poll: true)
        tool 'ADOP Maven'
        sh 'mvn clean install -DskipTests'
      }
    }
  }
  environment {
    WORKSPACE_NAME = 'MDC'
    PROJECT_NAME = 'MDC/DEMO'
  }
}