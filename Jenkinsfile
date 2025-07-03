pipeline {
    agent any

    tools {
        maven 'Maven 3.9.6' // Remplace par le nom exact que tu as configuré dans Jenkins
        jdk 'Java 17'       // Remplace par la version que tu utilises
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/stuprog/jenkins-java-app.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
