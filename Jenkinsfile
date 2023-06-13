//Declarative Pipeline
pipeline { 
    agent any //requerido

    stages {
        stage('Instalar dependencies:'){
            steps {
                bat "npm install"
            }
        }
    
        stage('Compilar la aplicacion: '){
            steps {
                bat "npm run build"
            }
        }
    }

}
