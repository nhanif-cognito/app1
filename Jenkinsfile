pipeline {
    agent any
    stages {
        stage('test slaves') {
            steps {
                script {
                    def jobs = [:]

                    jobs['1'] = { node('default') { echo 'successfully started a standard slave' } }
                    jobs['2'] = { node('default') { echo 'successfully started a standard slave' } }
                }
            }
        }
    }
}
