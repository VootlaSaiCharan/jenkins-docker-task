pipeline {
    agent any

    stages {
        stage('Git') {
            steps {
                script {
                    // Build Docker image
                    git 'https://github.com/VootlaSaiCharan/jenkins-docker-task.git'
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    // Run tests if needed
                    sh 'sudo -S docker build -t pythonlinux .'
                }
            }
        }

        stage('Run') {
            steps {
                script {
                    // Deploy the Docker image as needed
                    sh 'sudo -S docker run -it pythonlinux'
                }
            }
        }
    }
}
