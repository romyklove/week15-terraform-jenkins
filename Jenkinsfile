pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('test') {
            steps {
                echo 'Hello test'
            }
        }
         stage('package') {
            steps {
                echo 'Hello package'
            }
        }
    }
}

*** Jenkinsfile for terraform code

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

 
