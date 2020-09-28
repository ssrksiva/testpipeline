pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo $DOCKER_HOME'
      }
    }

  }
  environment {
    DOCKER_HOME = ' tool \'docker\''
  }
}