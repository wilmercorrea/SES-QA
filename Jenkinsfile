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
    stage('JIRA') {
      steps {
        jiraTransitionIssue(idOrKey: 'GSDCI-1', site: 'https://servicesolutions.atlassian.net/', input: '10100', auditLog: true, failOnError: true)
      }
    }
  }
  environment {
    label = 'Builder'
  }
}