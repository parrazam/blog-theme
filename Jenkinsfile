pipeline {
  agent any 
  tools {
    nodejs "node-16.x.y"
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
      }
    }
    stage('create zip file') { 
      steps {
        sh 'rm -rf node_modules'
        sh 'yarn cache clean'
        sh 'yarn install'
        sh 'yarn zip'
      }
    }
  }
}
