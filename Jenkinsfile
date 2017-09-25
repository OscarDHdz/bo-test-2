pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''echo \'Hello World\'
echo $PROJECT_NAME'''
        git(url: 'ssh://jenkins@gerrit:29418/MDC/DEMO/demo-base-spring-petclinic', branch: 'master', credentialsId: 'adop-jenkins-master', poll: true)
        tool(name: 'ADOP Maven', type: '3.0.5')
        sh 'mvn clean'
      }
    }
  }
  environment {
    WORKSPACE_NAME = 'MDC'
    PROJECT_NAME = 'MDC/DEMO'
  }
}