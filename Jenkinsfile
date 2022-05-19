pipeline{
    agent any
    stages{
        stage('Build da imagem docker'){
            steps{
                sh 'docker build -t devops/app'
            }
        }
        stage('Subir docker-compose - redis e app'){
            steps{
                sh 'docker-compose up --build -d'
            }
        }
        stage('sleep para levantar o container'){
            steps{
                sh 'sleep 30'
            }
        }
        stage('teste da aplicação'){
            steps{
                sh 'teste-app.sh'
            }
        }
    }
}