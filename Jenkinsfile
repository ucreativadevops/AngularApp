pipeline{
    agent any

    stages{
        stage('Instalar dependencias'){
            steps{
                sh 'npm install'
            }
        }

        stage('Compilacion del App'){
            steps{
                sh 'npm run build'
            }
        }

        stage('Mostrar los archivos'){
            steps{
                sh 'ls -la'
            }
        }

    }
}