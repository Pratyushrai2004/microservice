pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat '.\\gradlew.bat build'
            }
        }
        stage('Test') {
            steps {
                bat '.\\gradlew.bat test'
            }
        }
    }
}
