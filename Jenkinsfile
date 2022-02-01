pipeline {
    agent any

    stages {
        stage ("checkout from GIT") {
            steps {
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/vinay5898/tff.git'
            }
        }
        stage ("terraform init") {
            steps {
                sh 'sudo terraform init'
            }
        }
        stage ("terrafrom plan") {
            steps {
                sh 'sudo terraform plan '
            }
        }
        stage ("terraform apply") {
            steps {
                sh 'sudo terraform apply --auto-approve'
            }
        }
    }
}
