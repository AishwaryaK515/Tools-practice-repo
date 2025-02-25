pipeline {
    agent any
    tools { maven 'Maven-3' }  // Use the configured Maven installation

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'master', url: 'https://github.com/AishwaryaK515/tools.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
            }
        }
    }
}

