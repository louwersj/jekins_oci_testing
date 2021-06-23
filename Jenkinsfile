pipeline {
  agent any
  stages {
    stage('Initiate stage') {
      steps {
        echo 'Start initiate stage'
        sh '''#!/bin/bash
echo "haha"'''
      }
    }

    stage('repo analysis') {
      steps {
        echo 'Starting the analysis of what is in the repository we retrieved from version control'
      }
    }

  }
}