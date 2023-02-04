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
               git credentialsId: 'github',
               url: 'https://github.com/pradyumna93/react_django_demo_app.git',
               branch: 'main' 
            }
        }
        stage('Build Docker Image'){
            steps{
                script{
                    docker_image = docker.build "${Image_Name}"
                }
            }
        }
        stage('Push Docker image')
            steps{
                script{
                    docker.withRegistry('',Registry_Credintial){
                    docker_image.Push("$Image_name")
                }
            }
        }
    }
    
}