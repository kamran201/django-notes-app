pipeline {
    agent any

    stages{
        stage('cloning'){
            steps{
                echo 'this is cloning the code'
                git url:'https://github.com/kamran201/django-notes-app.git',branch:'main'
                echo 'code clone successfully done'
            }
        }
        stage('making a docker image'){
            
            steps{
                echo 'creating docker image'
                sh 'docker build -t notes-app . '
                echo 'image create succesful'
                
            }
        }
        stage('DEPLOYING '){
            steps{
                echo 'this is deploying the code'
                sh 'docker run -d -p 8000:8000 notes-app'
                echo'deploying successfully '
                
            
            }
        }
    }
}
