pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo \'Hello World\''
        git(url: 'ssh://jenkins@gerrit:29418/MDC/DEMO/demo-base-spring-petclinic', branch: 'master', credentialsId: 'adop-jenkins-master', poll: true)
      }
    }
  }
}