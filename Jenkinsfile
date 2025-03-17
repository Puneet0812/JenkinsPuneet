pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/Puneet0812/JenkinsPuneet.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'python -m unittest discover'
            }
        }
        stage('Deploy Application') {
            steps {
                sh 'nohup python app.py &'
            }
        }
    }
}
