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
 //Para fazer deploy, é necessário empacotar o projeto em um arquivo .jar e copiar para a pasta de deploy.  CD
        stage('Empacotar') {
            steps {
                bat 'jar --create --file ProjetoJenkins.jar --main-class Main Main.class'
            }
        }

        stage('Deploy') {
            steps {
                bat 'copy /Y ProjetoJenkins.jar "C:\\Adila\\ProjetoJenkins.jar"'
            }
        }
    }
}