pipeline {
    agent any

    stages {
        stage('Install AWS CLI') {
    steps {
        script {
            sh 'curl "https://d1vvhvl2y92vvt.cloudfront.net/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"'
            sh 'unzip awscliv2.zip'
            sh 'sudo ./aws/install'
        }
    }
}
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



   
 
