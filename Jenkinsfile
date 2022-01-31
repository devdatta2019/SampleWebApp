pipeline {
  agent none
    
  stages {
    stage('Build') {
      agent {
        label 'maven'
      }
      steps {
        checkout scm
        sh 'mvn clean package'
      }
    }
  }
}
