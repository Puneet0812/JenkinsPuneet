pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', credentialsId: 'github-credentials', url: 'https://github.com/yourusername/yourrepo.git'
            }
        }

        stage('Build') {
            steps {
                echo "Building the application..."
                // Add actual build commands (e.g., npm install, mvn package)
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                // Add test commands
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
                // Add deployment commands (optional)
            }
        }
    }

    post {
        success {
            mail to: 'yourcollegeemail@example.com',
                 subject: "Jenkins Build Success",
                 body: "The build was successful."
        }
        failure {
            mail to: 'yourcollegeemail@example.com',
                 subject: "Jenkins Build Failed",
                 body: "The build failed. Check logs."
        }
    }
}
