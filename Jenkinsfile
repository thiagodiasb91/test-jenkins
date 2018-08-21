pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                bat './gradlew check'
            }
        }
    }
    post {
        always {
            junit 'build/reports/**/*.xml'
        }
    }
}