pipeline {
  agent { label 'maven' }
  stages {
    stage('build') {
      steps {
        sh 'echo Building ${BRANCH_NAME}...'
        sh 'ls -la'
        sh 'cd ./complete && ls -la'
        sh 'mvn clean compile'
        sh 'mvn test'
      }
    }
  }
}