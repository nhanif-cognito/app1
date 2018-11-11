// pipeline to create image using Dockerfile and tag new image.
pipeline {
	  agent { dockerfile true }
		options {
        ansiColor('xterm')
        timestamps()
        buildDiscarder(logRotator(numToKeepStr:'50'))
    }
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
