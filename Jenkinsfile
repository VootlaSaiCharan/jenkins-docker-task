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
                    sh 'docker build -t pythonlinux /var/lib/jenkins/workspace/jenkins-docker/'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Deploy the Docker image as needed
                    sh 'docker run -it pythonlinux'
                }
            }
        }
    }
}
