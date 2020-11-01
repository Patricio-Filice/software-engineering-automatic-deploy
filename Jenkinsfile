pipeline {
  agent any
  stages {
    stage('Grant Permissions') {
      steps {
        sh 'chmod +x gradlew'
      }
    }

    stage('Build') {
      steps {
        sh './gradlew build'
      }
    }

    stage('Test') {
      steps {
        sh './gradlew test'
      }
    }

    stage('Analyze') {
      steps {
        sh './gradlew sonarqube'
      }
    }

    stage('Validate') {
      steps {
        sh 'echo "Validated"'
      }
    }

    stage('Deply') {
      steps {
        sh '''./gradlew bootRun
echo "Deployed"'''
      }
    }

  }
}