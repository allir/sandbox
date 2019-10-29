pipeline {
  agent any
  
  stages {
    stage('Environment'){
      steps{
        sh 'env'
        sh 'echo ${GIT_COMMIT}'
        sh 'git rev-parse --short ${GIT_COMMIT}'
      }
    }
  }
}
