pipeline {
    agent any

    stages {
        stage('initialize') {
            steps {
                sh 'terraform init'
            }
        }
        stage('format') {
            steps {
               sh 'terraform fmt'
            }
        }
         stage('validate') {
            steps {
                sh 'terraform validate'
            }
        }
         stage('AWS Configure') {
            steps {
                script {
                    sh 'aws configure set aws_access_key_id AKIASWR35KIAOKYOSCMN'
                    sh 'aws configure set aws_secret_access_key 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'
                    sh 'aws configure set region us-east-1'
                }
            }
        }
     stage('plan') {
            steps {
                sh 'terraform plan'
            }
        }
        stage('apply') {
            steps {
                sh 'terraform apply --auto-approve'
            }
        }
    }        
}



   
 
