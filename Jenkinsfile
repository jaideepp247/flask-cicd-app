pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/jaideepp247/flask-cicd-app.git/', branch: 'master'
            }
        }
        stage('Build') {
            steps {
                sh 'docker build -t flask-ci-cd-project .'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Running tests..."'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker run -d -p 5000:5000 flask-ci-cd-project'
            }
        }
    }
}
