pipeline {
  agent any 
  tools {
    nodejs "node-14.16.1"
  }
  options {
    skipStagesAfterUnstable()
  }
  stages {
    stage('Build') { 
      steps {
        sh 'node -v'
        sh 'npm -v'
        // sh 'npm install yarn'
        sh 'yarn install' 
      }
    }
    stage('create zip file') { 
      steps {
        sh 'rm -rf node_modules'
        sh 'yarn cache clean'
        sh 'yarn zip'
      }
    }
  }
}
