pipeline {
    agent any

    environment {
        // Définir le chemin de Maven (ajustez-le selon votre installation)
        mvnHome = 'C:/Program Files (x86)/apache-maven-3.9.9-bin/apache-maven-3.9.9'
    }

    stages {
        stage('Checkout') {
            steps {
                // Cloner le code depuis le dépôt Git
                git 'https://github.com/Samba-SISSOKO/projet_jenkins.git'
            }
        }

        stage('Build') {
            steps {
                // Construire le projet
                bat "\"${mvnHome}/bin/mvn\" clean install"
            }
        }

        stage('Test') {
            steps {
                // Exécuter les tests
                bat "\"${mvnHome}/bin/mvn\" test"
            }
        }
    }
}
