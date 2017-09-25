pipeline {
  agent {
    node {
      label 'java8'
    }
    
  }
  stages {
    stage('Initialize') {
      steps {
        git(url: 'ssh://jenkins@gerrit:29418/MDC/DEMO/demo-base-spring-petclinic', branch: 'master', credentialsId: 'adop-jenkins-master', poll: true)
        node(label: 'java8') {
          sh '''echo "PATH = ${PATH}"
echo "M2_HOME = ${M2_HOME}"
mvn clean install'''
        }
        
      }
    }
  }
  environment {
    WORKSPACE_NAME = 'MDC'
    PROJECT_NAME = 'MDC/DEMO'
  }
}