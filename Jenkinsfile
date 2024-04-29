pipeline {
    agent any

    environment {
        AWS_ACCESS_KEY_ID     = credentials('aws-access-key-id')
        AWS_SECRET_ACCESS_KEY = credentials('aws-secret-access-key')
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/KeerthuK29/Terraform_RDS.git'
            }
        }
        stage('Run') {
            steps {
                dir('C:\\Users\\kesavank\\Terraform'){

                    bat'terraform init'
                    bat 'terraform plan'
                    bat 'terraform apply -auto-approve'
 
                   }
            }
                
         
            }
        }
    }
