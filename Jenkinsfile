pipeline {
    agent any
    stages {
        stage('Build') {
        steps {
            bat 'echo "Building project..."'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }

    }
}