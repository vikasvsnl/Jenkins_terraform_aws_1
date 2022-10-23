pipeline{
    agent any
    tools {
        terraform 'jenkins-terraform'
        }
    stages {
        stage('checkout from GIT') {
            steps {
                git branch: 'main', credentialsId: '2ec5da10-6c6f-4f7b-b86b-ae6096f13ad3', url: 'https://github.com/vikasvsnl/Jenkins_terraform_aws_1' 
            }
        }
        stage('terraform init') {
            steps {
                sh 'terraform init'
            }
        }
        stage('terraform fmt') {
            steps {
                sh 'terraform fmt'
            }
         }   
        stage('terraform vaidate') {
            steps {
                sh 'terraform validate'
            }
         }
         stage('terraform plan') {
            steps {
                sh 'terraform plan'
            }
        }
    }
}
