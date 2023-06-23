pipeline{
    agent any

environment {
        correos = 'devopschrisrd@gmail.com'
    }
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
        post{
          always{
            emailext body: "Notificacion de cambio Jenkins", subject: "Jenkins update", to: "${correo}"

      }
    }
}