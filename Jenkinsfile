pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/kavyashree123-ops/my-python-app.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t mypythonapp .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 5000:5000 --name python-container mypythonapp'
            }
        }

    }
}
