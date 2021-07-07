pipeline {
  agent {
    node {
      label 'intTempl_acceptance'
    }

  }
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
      steps {
        echo 'start code analysis 1'
      }
    }

    stage('build') {
      parallel {
        stage('Build') {
          steps {
            echo 'CA1.1'
          }
        }

        stage('Build x86') {
          agent {
            node {
              label 'buildAgentX86'
            }

          }
          steps {
            sh '''echo "hello world"
uname -a'''
          }
        }

        stage('Build ARM') {
          agent {
            node {
              label 'buildAgentArm64'
            }

          }
          steps {
            sh '''echo "hello world"
uname -a'''
          }
        }

      }
    }

  }
}