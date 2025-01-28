pipeline {
    agent any

    stages {
        stage('clone') {
            steps {
              git branch: 'main', url: 'https://github.com/CloudTechDevOps/Terraform_CICD.git'
            }
        }
        stage('init') {
            steps {
                sh 'terraform ${action}'
            }
        }
         stage('plan') {
            steps {
                sh 'terraform plan'
            }
        }
    }
}
