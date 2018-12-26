pipeline {
    agent {
        node {
            label 'master'
            }
          }
    stages {
        stage('Checkout'){
            steps {
                /* checkout scm */
                git branch: '${BRANCH_NAME}', credentialsId: 'a26c7a5c-3771-46e0-8676-6ac7ea1ebed8', url: 'https://github.com/thehouk/test-ni.git'
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
