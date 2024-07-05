pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'echo building'
                sh 'pip3 install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                sh 'echo testing'
                sh 'python3 manage.py test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo deploying'
                sh 'ssh aditya@44.204.68.222 -o StrickHostkeyChecking=no'
            }
        }
    }
}
