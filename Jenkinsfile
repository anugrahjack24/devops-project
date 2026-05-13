pipeline {
    agent any

    tools {
        maven 'Maven 3.9'
    }

    stages {

        stage('Clone') {
            steps {
                git branch: 'main',
                url: 'https://github.com/anugrahjack24/devops-project.git'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Verify') {
            steps {
                bat 'dir target'
            }
        }
    }
}
