pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                retry(3) {
                    bat './flakey-deploy.sh'
                }

                timeout(time: 3, unit: 'MINUTES') {
                    bat './health-check.sh'
                }
            }
        }
    }
}