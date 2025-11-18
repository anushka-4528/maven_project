pipeline {
    agent any

    tools {
        jdk 'jdk17'
        maven 'maven3'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/anushka-4528/maven_project.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment step (dummy for exam)'
            }
        }
    }

    post {
        success {
            echo 'Build Success!'
        }
        failure {
            echo 'Build Failed!'
        }
    }
}
