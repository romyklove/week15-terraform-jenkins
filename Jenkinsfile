pipeline {
    agent any

    stages {
        stage('initialize') {
            steps {
                sh 'terraform init'
            }
        }
        stage('format the code') {
            steps {
                sh 'terraform fmt'
            }
        }
         stage('validate') {
            steps {
                sh 'terraform validate'
            }
        }
        stage('format the code') {
            steps {
                sh 'terraform fmt'
            }
        }
         stage('plan') {
            steps {
                sh 'terraform plan'
    }
}
stage('format the code') {
            steps {
                sh 'terraform fmt'
            }
        }
         stage('apply') {
            steps {
                sh 'terraform apply --auto-approve'
  }
}
    }        
                
