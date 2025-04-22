pipeline {
    agent any

    stages {
        stage('Install MkDocs') {
            steps {
                sh 'pip install mkdocs'
            }
        }

        stage('Build README') {
            steps {
                sh 'mkdocs build'
            }
        }

        stage('Archive Site') {
            steps {
                archiveArtifacts artifacts: 'site/**', fingerprint: true
            }
        }
    }
}
