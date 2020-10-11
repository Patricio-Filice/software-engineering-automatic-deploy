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

  }
}