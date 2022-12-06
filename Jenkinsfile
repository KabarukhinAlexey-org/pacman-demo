pipeline{
    agent any
    options{
        buildDiscarder(logRotator(numToKeepStr: '5', daysToKeepStr: '5'))
        timestamps()
    }
    environment{
        
        registry = "docker.io/akabarukhin/pacman-demo"
        registryCredential = dockerhub-creds
    }
    
    stages{
       stage('Building image') {
      steps{
        script {
          dockerImage = docker.build registry
        }
      }
    }
       stage('Deploy Image') {
      steps{
         script {
            docker.withRegistry( '', registryCredential ) {
            dockerImage.push()
          }
        }
      }
    }
}
