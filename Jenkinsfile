pipeline {
    agent any

    tools {
        nodejs "NodeJS"
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'test',
                    url: 'https://github.com/ShanmukYadav/fullstack.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                dir('fullstack') {
                    sh 'npm install'
                }
            }
        }

        stage('Run Tests') {
            steps {
                dir('fullstack') {
                    sh 'npm test'
                }
            }
        }
    }
}
