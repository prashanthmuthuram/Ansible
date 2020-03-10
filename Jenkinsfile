pipeline {
    agent any
    tools {terraform "Terraform01221"}

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/PrasadTelasula/Ansible.git'
            }
            
        }

        stage('Terraform-Version-Check') {
            steps {
                sh 'terraform --version'
            }
        }

        stage('Terraform Init') {
            steps {
                sh 'terraform init'
            }
        }

        stage('Terraform Validate') {
            steps {
                sh 'terraform validate'
            }
        }

        stage('Terraform Plan') {
            steps {
                sh 'terraform plan'
            }
        }

        stage('Terraform Apply') {
            steps {
                sh 'terraform apply -auto-approve'
            }
        }
    }
}