pipeline {
  agent any
  stages {
    stage('Initialize') {
      steps {
        git(url: 'ssh://jenkins@gerrit:29418/MDC/DEMO/demo-base-spring-petclinic', credentialsId: 'adop-jenkins-master', branch: 'master')
        node(label: 'java8') {
          tool 'ADOP Maven'
          sh '''echo "PATH = ${PATH}"
echo "M2_HOME = ${M2_HOME}"'''
          sh 'whoami'
          sh 'uname -a'
          sh 'java -version'
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