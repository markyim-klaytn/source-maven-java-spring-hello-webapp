pipeline {
  agent any

  triggers {
    pollSCM('* * * * *')
  }

  stages {
    stage('Checkout') {
      steps {
        git branch: 'main', 
        url: 'http://3.38.200.252:8080/'
      }
    }
    stage('Build') {
      steps {
        echo 'hello world'
      }
    }
    stage('Test') {
      steps {
        echo 'hello world'
      }
    }
    stage('Deploy') {
      steps {
        deploy adapters: [tomcat9(credentialsId: '<NAME>', url: '<URL>')], contextPath: null, war: 'path/to/war'
      }
    }
  }
}
