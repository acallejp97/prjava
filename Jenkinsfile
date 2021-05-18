pipeline {
    agent any

    stages {
        stage('Compilar fichero') {
            steps {
                sh 'javac Simple.java'
            }
        }
        stage('Ejecutar fichero') {
            steps {
                sh 'java Simple'
            }
        }
    }
}
