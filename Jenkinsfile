use below commands to run the build

// usermod -aG docker jenkins
// usermod -aG root jenkins
// chmod 664 /var/run/docker.sock



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
                    sh 'docker build -t pythonlinux .'
                }
            }
        }

        stage('Run') {
            steps {
                script {
                    // Deploy the Docker image as needed
                    sh 'docker run -i pythonlinux'
                }
            }
        }
    }
}
