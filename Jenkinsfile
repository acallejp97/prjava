pipeline {
    agent any

    environment{
        nombre="${variable1}"
	maquina="""${sh(
			returnStdout: true,
			script: 'uname -n'
                      )
		    }"""
    }
    stages {
        stage('Compilar fichero Simple') {
            steps {
                sh 'javac Simple.java'
            }
        }
        stage('Ejecutar fichero Simple') {
            steps {
                sh 'java Simple ${nombre}'
            }
        }
        stage('Compilar fichero Param') {
            steps {
                sh 'javac Param.java'
            }
        }
        stage('Ejecutar fichero Param') {
            steps {
                sh 'java Param ${nombre}'
            }
        }
	stage('nombreMaquina'){
	   steps{
               echo "Y aquí visualizeo el nombre de la maquina "
	       sh 'javac Maquina.java'
               sh 'java Maquina ${maquina}'
           }
       }
    }
}
