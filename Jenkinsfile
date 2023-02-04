pipeline {
    agent any
    environment{
        Dockerhub_username = "pradyumna93"
        App_name = "Django_todo_app"
        Image_tag = "${Build_number}"
        Image_name = "${Dockerhub_username}" + "/" + "${App_name}"
        Registry_Credintial = "dockerhub"
    }
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