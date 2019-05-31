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
        sh 'which -a mvn'
      }
    }

    stage('Kubernetes Test'){
      steps{
        container('maven'){
          sh 'hostname'
          sh 'env'
          sh 'which -a mvn'
        }
      }
    }
  }
}
