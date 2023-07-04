pipeline{
    agent {
        label "linux-agent"
    }

    stages{

        stage("Confirmación despliegue"){
            input{
                message "¿Desea comenzar el despliegue?"
                ok "Si"
            }
            steps{
              echo "Comenzando deploy"
            }
        }

        stage("Instalación de dependencias"){
            steps{
                sh "npm install"
            }
        }
        
        stage ("Prueba unitaria"){
            steps{
                echo "Comando de las pruebas unitarias npm run test"
            }
        }
/*
        stage('Pruebas de seguridad-sonarqube'){
            steps{
                withSonarQubeEnv('SonarQubeCursoCI'){
                    sh "/opt/sonar-scanner/bin/sonar-scanner -Dsonar.projectKey=AngularApp"
                }
            }
        }*/

        stage ("Compilación de la aplicación"){
            steps{
                sh "npm run build"
            }
        }

        /*post{
            success {
                emailext body: "La prueba ha finalizado con exito", subject: "Aviso", to: "josecursoci@gmail.com"
            }
            failure {
                emailext body: "La prueba no finalizo con exito", subject: "Aviso", to: "josecursoci@gmail.com"
            }
        }*/

        /*
        when (branch 'dev'){
            steps{
                sh 'scp dist/AngularApp/* root@206.189.254.187:/usr/ucreativa/jose-dev/'
            }
        }
        when (branch 'staging'){
            steps{
                sh "scp dist/AngularApp/* root@206.189.254.187:/usr/ucreativa/jose-staging/"
            }
        }
        when (branch "main"){
            steps{
                sh "scp dist/AngularApp/* root@206.189.254.187:/usr/ucreativa/jose-prod/"
            }
        }
        */
    }

    post{
        success {
            emailext body: "La prueba fue exitosa", subject: "Aviso", to: "josecursoci@gmail.com"
        }
        failure {
            emailext body: "La prueba tuvo un fallo", subject: "Aviso", to: "josecursoci@gmail.com"
        }
     }

    
}
