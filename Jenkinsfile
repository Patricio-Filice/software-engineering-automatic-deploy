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

    stage('Validate') {
      steps {
        sh 'echo "Validated"'
      }
    }

    stage('Deploy') {
      steps {
        sh '''./gradlew bootRun
echo "Deployed"'''
      }
    }

  }
}