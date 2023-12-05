pipeline {
  agent {
      label "jenkins-node"
    }
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
        sh 'mvn clean package'
      }
    }
    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }
    stage('Deploy') {
      steps {
        deploy adapters: [tomcat9(credentialsId: '3ce143c1-7c97-41fb-a2fc-f5a8be7cc42a', path: '', url: 'http://3.38.200.252:8080/')], contextPath: '/hello-world', war: 'target/hello-world.war'
      }
    }
  }
}
