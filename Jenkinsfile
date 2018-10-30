// pipeline to create image using Dockerfile, tag it before pushing to Docker Hub.
pipeline {
	  agent { dockerfile true }
  stages {
		stage('Test') {
      steps{
          echo 'successfuly build latest image'
      }
    }
	}
  post {
		success {
        echo 'built successfull'
		}
  }
}
