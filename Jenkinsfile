pipeline {
    agent any

    stages {

        stage('Compilar') {
            steps {
                bat 'javac Main.java'
            }
        }

        stage('Executar') {
            steps {
                bat 'java Main'
            }
        }
    }
}