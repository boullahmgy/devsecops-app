pipeline {
    agent any

    environment {
        APP_NAME = "devsecops-app"
        IMAGE_NAME = "devsecops-app:latest"
        CONTAINER_NAME = "next-app"
        APP_PORT = "3000"
    }

    stages {

        stage('Checkout') {
            steps {
                echo 'Récupération du code source...'
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                echo 'Installation des dépendances...'
                sh 'npm install'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Analyse de sécurité des dépendances...'
                sh 'npm audit --audit-level=high || true'
            }
        }

        stage('Docker Build') {
            steps {
                echo 'Construction de l’image Docker...'
                sh 'docker build -t $IMAGE_NAME .'
            }
        }

        stage('Deploy Container') {
            steps {
                echo 'Déploiement du conteneur...'
                sh '''
                docker rm -f $CONTAINER_NAME || true
                docker run -d \
                --restart unless-stopped \
                --name $CONTAINER_NAME \
                -p $APP_PORT:$APP_PORT \
                $IMAGE_NAME
                '''
            }
        }

        stage('Health Check') {
            steps {
                echo 'Vérification de l’application...'
                sh '''
                sleep 10
                curl -f http://localhost:$APP_PORT || exit 1
                '''
            }
        }

        stage('Notification') {
            steps {
                echo 'Pipeline terminé avec succès.'
            }
        }
    }

    post {
        success {
            echo '✅ Pipeline DevSecOps exécuté avec succès.'
        }

        failure {
            echo '❌ Pipeline DevSecOps échoué.'
        }
    }
}
