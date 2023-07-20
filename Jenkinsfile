pipeline{
    agent any
    
    stages{
        stage("clone code"){
            steps {
                echo "cloning the code from github"
                git url: "https://github.com/Tripti-TD/django-notes-app-DevOps.git", branch:"main"
            }
        }
        stage("build code"){
            steps {
                echo "building the docker image"
                sh "docker-compose down && docker-compose up -d"
            }
            
        }
        stage("push to dockerhub"){
            steps {
                echo "pushing to docker hub"
                withCredentials([usernamePassword(credentialsId:"dockerhub", passwordVariable:"dockerhubPass",usernameVariable:"dockerhubUser")]){
                /*sh "docker tag my-note-app ${env.dockerhubUser}/my-note-app:latest"*/
                sh "docker login -u ${env.dockerhubUser} -p ${env.dockerhubPass}"
                sh "docker push ${env.dockerhubUser}/my-note-app:latest"
                }
            
            }
            
        }
        stage("Deploy container"){
            steps {
                echo "Deploying the container"
                sh "docker-compose down && docker-compose up -d"
            }
            
        }
    }
}
