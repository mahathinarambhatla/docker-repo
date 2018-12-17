pipeline {
    agent any
    def app
    stages {
        stage('Test') {
            steps {
                 app = docker.build()
              }
        }
    }
}
