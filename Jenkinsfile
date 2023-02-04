pipeline {
    agent any

    stages{
        stage('Git Checkout SCM'){
            steps{
               git url: 'https://github.com/pradyumna93/react_django_demo_app.git'
            }
        }
        stage('Build Docker Image'){
            steps {
                sh "docker build -t pradyumna93/Djano_App:1.0"
            }
    }
    
}
}