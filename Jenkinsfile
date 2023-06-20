pipeline {
    agent any

    stages {
        
<<<<<<< Updated upstream
        stage('Descargar Codigo') {
=======
        stage('Instalar dependencias') {
>>>>>>> Stashed changes
            steps {
                bat 'npm install'
            }
        }
        
      
<<<<<<< Updated upstream
        stage('Despliegue en Ambiente de Desarrollo') {
            steps {
                bat 'npm run build'
=======
        stage('Compilacion del APP') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Mostrar Archivos') {
            //when {branch 'dev'}
            steps {
                sh 'ls -la'
>>>>>>> Stashed changes
            }
        }
    }
}