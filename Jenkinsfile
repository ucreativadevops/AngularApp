pipeline {
    agent any

    stages {
        
        stage('Descargar Codigos') {
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