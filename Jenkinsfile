pipeline {
    agent any
    
    stages {
        stage('Test') {
            def app
            steps {
                 app = docker.build "your-project-name"
              }
        }
    }
}
