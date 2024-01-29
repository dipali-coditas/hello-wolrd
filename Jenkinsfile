pipeline {
    agent any

    stages {
        stage("Clone Code") {
            steps {
                echo "Cloning the code"
                git url: "https://github.com/dipali-coditas/hello-wolrd.git", branch: "main"
            }
        
        stage("Configure") {
            steps {
                script {
                    sh "sudo apt-get update"
                    sh "sudo apt-get install apache2 -y"
                    sh "sudo systemctl status apache2"
                }
            }
        }
        stage("Deploy") {
            steps {
                script {
                    sh "cd /var/www/html"
                    sh "sudo rm index.html"
                }
            }
        }
    }
}
