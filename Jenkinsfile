def isPr() {
    env.CHANGE_ID != null
}

pipeline {
  agent { label 'maven' }
  stages {
      stage('Init'){
          steps {
            echo 'Hello on ${BRANCH_NAME}...'
            echo 'printenv'
          }
          
      }
      stage('Build & Test'){
         when {
             expression { env.CHANGE_ID != null }
         } 
         steps {
            sh 'echo Building ${BRANCH_NAME}...'
            dir ('./complete'){
                sh 'mvn clean compile'
                sh 'mvn test'
            }
         }
      }
      stage('Change on master ') {
          when {
              branch 'master'
          }
          steps {
              echo 'Deployment to master'
          }
      }
  }
}
