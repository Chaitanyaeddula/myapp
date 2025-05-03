pipeline {
  agent any
  tools {
    maven 'Maven 3'
  }
  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/your-username/your-repo.git'
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
        echo 'Deploying Java App...'
      }
    }
  }
  post {
    success {
      echo 'Build Succeeded!'
    }
    failure {
      echo 'Build Failed.'
    }
  }
}

