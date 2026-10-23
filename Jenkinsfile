
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Construyendo la imagen Docker...'
                sh 'docker build -t lacteos-del-campo .'
            }
        }

        stage('Test') {
            steps {
                echo 'Comprobando la aplicación Python...'
                sh 'docker run --rm lacteos-del-campo'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Despliegue de demostración...'
                sh 'docker run --rm lacteos-del-campo'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completado correctamente.'
        }
        failure {
            echo 'El pipeline falló. Revisa la consola.'
        }
    }
}
