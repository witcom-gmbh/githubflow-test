pipeline {
  agent { label 'maven' }
  when {
    changeRequest()
    beforeAgent true
  }  
  stages {
    stage('build') {
      steps {
        sh 'echo Building ${BRANCH_NAME}...'
        dir ('./complete'){
            sh 'mvn clean compile'
            sh 'mvn test'
        }
      }
    }
  }
}
