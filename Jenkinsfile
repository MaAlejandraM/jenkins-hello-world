pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Compilando el código fuente...'
                sh 'ls -la'
            }
        }
        stage('Test') {
            steps {
                echo 'Ejecutando pruebas unitarias...'
                sh 'test -f index.html && echo "Prueba exitosa: index.html existe"'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Desplegando la aplicación en entorno de prueba...'
                sh 'mkdir -p deploy_env && cp index.html deploy_env/ && echo "Despliegue completado en deploy_env/"'
            }
        }
    }
}
