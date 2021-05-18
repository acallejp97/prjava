pipeline {
    agent any

    stages {
        stage('Compilar fichero') {
            steps {
                sh 'javac Param.java'
            }
        }
        stage('Ejecutar fichero') {
            steps {
                sh 'java Param ${variable1}'
            }
        }
    }
}
