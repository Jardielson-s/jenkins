pipeline {
    agent any

    tools {nodejs "node"}

    stages {
        stage('Git') {
            steps {
                git 'https://github.com/Jardielson-s/jenkins.git'
            }
        }

        stage('Build') {
            steps {
                sh 'npm install'
                 sh 'npm run build'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
    }
}