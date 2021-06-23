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

    stage('code analysis 1') {
      parallel {
        stage('code analysis 1') {
          steps {
            echo 'start code analysis 1'
          }
        }

        stage('code analysis 2') {
          steps {
            echo 'code analysis 2'
          }
        }

        stage('code analysis 3') {
          steps {
            echo 'code analysis 3'
          }
        }

      }
    }

    stage('CA1.1') {
      steps {
        echo 'CA1.1'
      }
    }

  }
}