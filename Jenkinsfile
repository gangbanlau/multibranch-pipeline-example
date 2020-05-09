#!/usr/bin/env groovy
node {
  stage('Checkout') {
    checkout scm
  }
  stage('Pre Build') {
    echo 'Pre build'
  }
  stage('Build') {
    echo 'Build'
  }
  stage('Test') {
    echo 'Test'
  }
  stage('Deploy') {
    echo 'branch name ' + env.BRANCH_NAME
    
    if (env.BRANCH_NAME.startsWith("Feature_")) {
      echo "Deploying to Dev environment after build"
      }
      
    else if (env.BRANCH_NAME.startsWith("Release_")) {
      echo "Deploying to Stage after build and Dev Deployment"
      }
      
    else if (env.BRANCH_NAME.startsWith("master")) {
      echo "Deploying to PROD environment"
      }
  }
}
