pipeline {
    agent any

    tools {
        jdk 'jdk-21'        // Nom exact de ton JDK configuré dans Jenkins
        maven 'Maven_3'     // Nom exact de ton Maven configuré dans Jenkins
    }

    stages {

        stage('Clone Git') {
            steps {
                // Clone du repo depuis Git
                git branch: 'main', url: 'https://github.com/doudousylla/mvn-helloworld.git'
            }
        }

        stage('Build') {
            steps {
                // Compilation + package Maven
                bat 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                // Exécution des tests Maven
                bat 'mvn test'
            }
        }

        stage('Run JAR') {
            steps {
                // Exécution du JAR généré
                bat 'java -jar target\\mvn-helloworld-1.0-SNAPSHOT.jar'
            }
        }
    }

    post {
        always {
            // Nettoyage du workspace après le build
            cleanWs()
        }
    }
}