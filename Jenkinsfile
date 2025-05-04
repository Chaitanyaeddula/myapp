pipeline {
  agent any
  tools {
    maven 'Maven 3'
    jdk 'JDK 21'
  }
  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/Chaitanyaeddula/myapp.git'
      }
    }
    stage('Build') {
      steps {
        sh 'mvn clean package'
      }
    }
  }
  post {
    always {
      echo 'Build completed'
    }
  }
}
