pipeline {
  environment {
    registry = "nhanif/hello-world"
    registryCredential = 'docker-hub'
    dockerImage = ''
  }
  agent any
  stages {
    stage('Clone repo') {
      steps {
        git 'https://github.com/nhanif-cognito/app1'
      }
    }  
    stage('Building image') {
      steps{
        script {
          dockerImage = docker.build registry + ":$BUILD_NUMBER"
        }
      }
    }
    stage('Deploy Image') {
      steps{
         script {
            docker.withRegistry( '', registryCredential ) {
            dockerImage.push()
          }
        }
      }
    }
  }
 post {
   success {
        echo 'built successfull'
   }
 }
}
