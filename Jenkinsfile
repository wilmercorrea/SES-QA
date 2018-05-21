pipeline {
  agent {
    node {
      label 'Builder'
    }

  }
  stages {
    stage('error') {
      steps {
        echo 'Hello Michelin'
        sh 'echo $HOSTNAME'
      }
    }
  }
  environment {
    label = 'Builder'
  }
}