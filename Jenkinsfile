pipeline {
    agent any

    tools {
        nodejs 'NodeJS 18' // Make sure you install NodeJS plugin and set it up in Jenkins
    }

    stages {
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test -- --watchAll=false'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy steps go here, e.g., copy to server or FTP'
            }
        }
    }
}
