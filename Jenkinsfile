pipeline {
    agent any

    stages{
        stage('Clone repository'){
            steps{
               git url: 'https://github.com/pradyumna93/react_django_demo_app.git'
            }
        }
        stage('Build Docker Image'){
            steps {
                sh "docker build"
            }
    }
    
}
}