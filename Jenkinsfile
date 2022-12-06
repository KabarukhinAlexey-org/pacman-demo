pipeline{
    agent any
    options{
        buildDiscarder(logRotator(numToKeepStr: '5', daysToKeepStr: '5'))
    }
    environment{
        registry = "docker.io/akabarukhin/pacman-demo"
        registryCredential = credentials('dockerhub-creds')
        def app
    }
    stages{
      stage('Building image') {
      steps{
        script {
          app = docker.build(registry)
          sh "env"
        }
      }
    }
  }
}
