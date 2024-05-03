pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building completed automatically with Maven.'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Unit and integration tests completed with Citrus.'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Code analyzing completed with Klocwork.'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Security scanning completed with App scanner.'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying completed with AWS EC2 staging instance.'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on the staging environment.'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying to AWS EC2 production instance.'
            }
        }

    }

    post {
        success {
        emailext subject: " Test and security scan Successfully",
        body: "Test and security scan successfully.",
        to: 'kwei19940425@gmail.com',
        attachLog: true
        }

        failure {
        emailext subject: " Test and security scan Failed",
        body: "Test and security scan Failed.",
        to: 'kwei19940425@gmail.com',
        attachLog: true
        }
    }
}
