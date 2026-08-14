pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/chittishivacharanreddy/test.git'
            }
        }

        stage('Build') {
            steps {
                bat 'set "PATH=C:\\Program Files\\apache-maven-3.9.16\\bin;%PATH%" && mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                bat 'set "PATH=C:\\Program Files\\apache-maven-3.9.16\\bin;%PATH%" && mvn test'
            }
        }
    }
}