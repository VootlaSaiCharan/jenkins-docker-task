pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Build Docker image
                    git 'https://github.com/VootlaSaiCharan/jenkins-docker-task.git'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Run tests if needed
                    sh 'sudo docker build -t pythonlinux .'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Deploy the Docker image as needed
                    sh 'sudo docker run -it pythonlinux'
                }
            }
        }
    }
}
