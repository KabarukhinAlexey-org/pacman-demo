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
      //agent {
      //  docker {
      //    image 'node:7-alpine'
      //    args '--name docker-node' // list any args
      //  }
      //}
      steps{
        script {
          sh "env && ls -lah"
            docker.withRegistry('docker.io', 'dockerhub-creds') {
            def app = docker.build("${registry}")
            app.push("${GIT_BRANCH}")
          }
        }
      }
    }
  }
}
