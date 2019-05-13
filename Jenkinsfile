pipeline {
  agent { label 'maven' }
  stages {
    stage('build') {
      steps {
        sh 'echo Building ${BRANCH_NAME}...'
<<<<<<< HEAD
        sh 'cd ./complete && mvn clean compile'
=======
        sh 'ls -la'
        sh 'cd ./complete && ls -la'
        sh 'mvn clean compile'
>>>>>>> refs/heads/feat-new-app
        sh 'mvn test'
      }
    }
  }
}