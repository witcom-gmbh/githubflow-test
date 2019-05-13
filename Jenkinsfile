pipeline {
  agent { label 'maven' }
  stages {
    stage('build') {
      when {
        changeRequest()
        beforeAgent true
      }  
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
