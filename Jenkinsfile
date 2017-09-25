pipeline {
  agent {
    docker {
      image 'maven:latest'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        sh '''echo \'Hello World\'
echo $PROJECT_NAME'''
        git(url: 'ssh://jenkins@gerrit:29418/MDC/DEMO/demo-base-spring-petclinic', branch: 'master', credentialsId: 'adop-jenkins-master', poll: true)
        sh 'mvn clean install -DskipTests'
      }
    }
  }
  environment {
    WORKSPACE_NAME = 'MDC'
    PROJECT_NAME = 'MDC/DEMO'
  }
}