pipeline {
    agent {
        node {
            label 'agent1'
            }
          }
    stages {
        stage('Checkout'){
            steps {
                /* checkout scm */
                git branch: '${BRANCH_NAME}', credentialsId: '7b8f5335-2f83-4e06-a80d-6b739328acfd', url: 'https://github.com/thehouk/test-ni.git'
                }
              }
        stage('Build'){
            steps {
                /* build image on remote machine */
                sh '''#!/bin/sh
                echo "Build Stage"'''
                }
              }
        stage('Test'){
            steps {
                /* build image on remote machine */
                sh '''#!/bin/sh
                echo "Test Stage"'''
                }
              }
        stage('Deploy'){
            steps {
                /* run container on remote machine */
                sh '''#!/bin/sh
                echo "Test Stage"'''
                  }
                }
              }
    post{
        success {
              echo 'whole pipeline successful'
                  }
        failure {
              echo 'pipeline failed, at least one step failed'
                   }
        }
}
