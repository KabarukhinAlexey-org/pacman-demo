pipeline{
    agent any
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
          def app = docker.build("${registry}")
          sh "env"
        }
      }
    }
  }
}
