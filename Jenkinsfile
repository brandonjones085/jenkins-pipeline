pipeline {
  agent any
  stages {
    stage('Install') {
      steps { sh 'npm install' }
    }

    stage('Test') {
      parallel {
        stage('Static code analysis') {
            steps { sh 'npm run-script lint' }
        }

      }
    }

    stage('Build') {
      steps { sh 'npm run-script build' }
    }
  }
}