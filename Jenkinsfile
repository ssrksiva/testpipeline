pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args '-v /root/.m2:/root/.m2'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn -B -DskipTests clean package'
      }
    }

  }
  environment {
    DOCKER_OPTS = '-H tcp://0.0.0.0:2376 -H unix:///var/run/docker.sock'
  }
}