pipeline {
  agent {
    node {
      label 'agent any'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'gradle build'
      }
    }

    stage('Test') {
      steps {
        sh 'gradle test'
      }
    }

    stage('Validate') {
      steps {
        sh 'echo "Validated"'
      }
    }

    stage('Deploy') {
      steps {
        sh '''gradle bootRun
echo "Deployed"'''
      }
    }

  }
}