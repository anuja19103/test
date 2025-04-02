pipeline {
    agent any  // Use any available agent (node)
    
    environment {
        // Optional: Define environment variables here if needed
        MY_ENV_VAR = 'some_value'
    }
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout code from SCM
                git 'https://github.com/yourusername/your-repo.git'
            }
        }

        stage('Build') {
            steps {
                // Run a simple build command, e.g., compiling Java code
                echo 'Building the project...'
                sh 'echo "Build step"'
                // Example: sh './gradlew build' for Gradle-based projects
            }
        }

        stage('Test') {
            steps {
                // Run tests if applicable
                echo 'Running tests...'
                // Example: sh './gradlew test'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy to a server or environment
                echo 'Deploying application...'
                // Example: sh './deploy.sh'
            }
        }
    }

    post {
        success {
            // Actions to take if the pipeline succeeds
            echo 'Pipeline finished successfully!'
        }

        failure {
            // Actions to take if the pipeline fails
            echo 'Pipeline failed!'
        }
    }
}
