pipeline {
    agent any

    environment {
        // Set environment variables if needed
        JAVA_HOME = "/usr/lib/jvm/java-11-openjdk"
        PATH = "${JAVA_HOME}/bin:${env.PATH}"
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from the Git repository
                git 'https://github.com/your-username/your-repository.git'
            }
        }

        stage('Build') {
            steps {
                // Run the build command (Maven in this case)
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // Run tests (can be unit tests, integration tests, etc.)
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                // Deployment step (for example, to AWS, Docker, etc.)
                echo 'Deploying application...'
                // Example: sh 'deploy.sh'
            }
        }
    }

    post {
        success {
            // Actions if the pipeline is successful
            echo 'Pipeline completed successfully!'
        }
        failure {
            // Actions if the pipeline fails
            echo 'Pipeline failed.'
        }
    }
}
