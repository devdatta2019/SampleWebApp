pipeline {
   agent {
      label "default"
   }
   stages {
      stage('Checkout') {
          steps {
            deleteDir()
            checkout scm
            }
         }
      }
      stage('Build') {
         agent {
            label "maven"
         }
         steps {
            sh 'mvn clean compile'
         }
      }
      stage('Test') {
         agent {
            label "maven"
         }
         steps {
            sh 'mvn test'
         }
      }
