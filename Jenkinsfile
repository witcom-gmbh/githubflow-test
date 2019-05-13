pipeline {
  agent { label 'maven' }
  stages {
    stage('build') {
      steps {
        sh 'echo Building ${BRANCH_NAME}...'
        sh 'cd ./complete && mvn clean compile '
        sh 'mvn test'
      }
    }
  }
}