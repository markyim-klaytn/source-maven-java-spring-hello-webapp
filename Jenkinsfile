pipeline {
  agent any

  triggers {
    pollSCM('* * * * *')
  }

  stages {
    stage('Checkout') {
      steps {
        git branch: 'main', 
        url: 'https://github.com/markyim-klaytn/source-maven-java-spring-hello-webapp'
      }
    }
    stage('Build') {
      steps {
        sh 'cat /etc/fstab'
      }
    }
    stage('Test') {
      steps {
        sh 'cat /etc/fstab'
      }
    }
    stage('Deploy') {
      steps {
        deploy adapters: [tomcat9(credentialsId: '<NAME>', url: '<URL>')], contextPath: null, war: 'path/to/war'
      }
    }
  }
}
