pipeline {
  agent maven
  stages {
    stage('build') {
      steps {
        sh 'echo Building ${BRANCH_NAME}...'
        sh 'cd ./complete'
        sh 'mvn clean compile'
        sh 'mvn test'
      }
    }
  }
}