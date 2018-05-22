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
    stage('two') {
      steps {
        sh 'node install --production'
      }
    }
  }
  environment {
    label = 'Builder'
  }
}