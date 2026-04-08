pipeline {
    agent any

    tools {
    maven 'Maven_home'
}

    stages {
        stage('Build') {
            steps {
                bat 'mvn clean test'
            }
        }
    }

    post {
        always {
            junit '**/target/surefire-reports/*.xml'
        }
    }
}