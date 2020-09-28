pipeline {
  agent {
    docker {
      image '\'maven:3-alpine\''
      args '\'-v /root/.m2:/root/.m2\''
    }

  }
  stages {
    stage('') {
      steps {
        sh '''echo $JAVA_HOME
echo $MAVEN_HOME'''
      }
    }

  }
  environment {
    JAVA_HOME = 'tool \'jdk8\''
    mvnHome = 'tool \'Maven 3.3.1\''
  }
}