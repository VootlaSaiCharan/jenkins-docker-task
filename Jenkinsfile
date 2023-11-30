pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Build Docker image
                    git clone https://github.com/VootlaSaiCharan/jenkins-docker-task.git
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Run tests if needed
                    docker build -t pythonlinux .
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Deploy the Docker image as needed
                    docker run -it pythonlinux
                }
            }
        }
    }
}