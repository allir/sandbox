pipeline {
  agent{
    kubernetes {
      label 'mypod'
      defaultContainer 'jnlp'
      yamlFile 'JenkinsPod.yaml'
    }
  }
  
  stages {
    stage('Environment'){
      steps{
        sh 'hostname'
        sh 'env'
      }
    }

    stage('Kubernetes Test'){
      steps{
        container('builder-base'){
          sh 'hostname'
          sh 'env'
        }
      }
    }
  }
}
