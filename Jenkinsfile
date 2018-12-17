pipeline {
    agent { dockerfile true }
    stages {
        stage('Test') {
            steps {
                sh 'whoami'
                sh 'python --version'
              }
        }
    }
}
