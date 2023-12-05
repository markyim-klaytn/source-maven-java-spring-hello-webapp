pipeline {
  agent any

  stages {
    stage('Parellel Job') {
      parellel{
        stage('parellel1'){
      steps {
        sh 'sleep 20'
        echo 'Hello World'
        echo 'Hello World Again
      }
    }
        stage('parellel2'){
      steps {
        sh 'sleep 20'
        sh 'cat /etc/os-release'
      }
    }
   }
  }
 }
}
