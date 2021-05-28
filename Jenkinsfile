pipeline {
  agent any 
  tools {
    nodejs "node"
  }
  options {
    skipStagesAfterUnstable()
  }
  stages {
    stage('Build') { 
      steps {
        sh 'node -v'
        sh 'npm -v'
        sh 'npm install -g yarn'
        sh 'yarn install' 
      }
    }
    stage('create zip file') { 
      steps {
        sh 'yarn zip'
      }
    }
  }
}
