pipeline {
  agent {
    node {
      label 'Builder'
    }

  }
  stages {
    stage('agent-def') {
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