pipeline {
    agent any

    stages {
        
        stage('Descargar Codigo!!') {
            steps {
                bat 'npm install'
            }
        }
        
      
        stage('Despliegue en Ambiente de Desarrollo!!') {
            steps {
                bat 'npm run build'
            }
        }
    }
}