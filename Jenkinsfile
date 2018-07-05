pipeline {
  agent any
  stages{
    stage('Build'){
      steps {
        sh 'clean package'
      }
      post {
        success {
            echo 'Now archiving ....'
            archiveArtifacts artifacts: '**/target/*.war'
        }
      }
    }
   }
}
