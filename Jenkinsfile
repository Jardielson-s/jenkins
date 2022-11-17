pipeline {
    agent any

    tools {nodejs "node"}

    stages {

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

        steps('Connect Ec2') {
            sshagent(credentials: ['EC2']) {
                sh 'ssh  ubuntu@ec2-3-80-51-90.compute-1.amazonaws.com'
            }
        }
    }
}