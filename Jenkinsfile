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
          sh 'java -version'
          sh '''MAVEN_HOME=/opt/maven 
PATH=$MAVEN_HOME/bin:$PATH'''
          sh 'ls /'
          sh 'ls /opt/'
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