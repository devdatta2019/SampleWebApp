pipeline {
  agent none
    
  stages {
    stage('Build') {
      agent {
        label 'kubeagent'
      }
      steps {
        checkout scm
        sh './mvnw -DskipTests clean package'
      }
    }
  }
}
