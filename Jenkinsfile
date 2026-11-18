pipeline {
  agent any
  environment {
    APP_NAME="Ex3"
  }
  stages {
    stage("First stage") {
      steps {
        sh 'echo "First stage"'
      }
    }
    stage("Failing step") {
      steps {
        pom
      }
    }
  }

  post {
    success { echo "OK." }
    failure { echo "Not OK." }
  }
}
