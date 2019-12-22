pipeline {
  agent any
  environment {
    branch = 'master'
    scmUrl = 'https://github.com/daikol68/daikol-pom'
  }
  stages {
    stage('checkout git') {
      steps {
        git branch: branch, credentialsId: 'GitCredentials', url: scmUrl
      }
    }

    stage('deploy'){
      steps {
        sh 'mvn deploy'
      }
    }
  }
}