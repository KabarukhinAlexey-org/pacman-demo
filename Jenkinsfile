pipeline{
    agent none
    options{
        buildDiscarder(logRotator(numToKeepStr: '5', daysToKeepStr: '5'))
    }
    environment{
        registry = "docker.io/akabarukhin/pacman-demo"
        registryCredential = credentials('dockerhub-creds')
    }
    stages{
      stage('Building image') {
      agent {
        docker {
          image 'node:7-alpine'
          args '--name docker-node' // list any args
        }
      steps{
        script {
          sh "env && ls -lah"
          def app = docker.build("${registry}")
        }
      }
    }
  }
}
