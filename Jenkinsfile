pipeline{
    agent {
        docker { image 'node:7-alpine' }
    }
    options{
        buildDiscarder(logRotator(numToKeepStr: '5', daysToKeepStr: '5'))
    }
    environment{
        registry = "docker.io/akabarukhin/pacman-demo"
        registryCredential = credentials('dockerhub-creds')
    }
    stages{
      stage('Building image') {
      steps{
        script {
          sh "env && ls -lah"
          def app = docker.build("${registry}")
        }
      }
    }
  }
}
