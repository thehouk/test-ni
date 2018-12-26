pipeline {
    agent {
        node {
            label 'master'
            }
          }
    stages {
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
