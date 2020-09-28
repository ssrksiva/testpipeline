pipeline {
  agent any
  stages {
    stage('CheckOut') {
      steps {
        git(url: 'https://github.com/ssrksiva/testpipeline.git', branch: 'master', credentialsId: '7c7c8f19-f795-43bf-999b-6c138d7ffa3d', poll: true)
      }
    }

    stage('Build') {
      steps {
        sh '${mvnHome}/bin/mvn clean package'
      }
    }

  }
  environment {
    JAVA_HOME = 'tool \'jdk8\''
    mvnHome = 'tool \'Maven 3.3.1\''
  }
}