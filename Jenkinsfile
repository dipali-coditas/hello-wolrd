pipeline {
  agent any 
  stages {
    stage("Clone Code") {
      steps {
        echo "Cloning code" 
        git branch: 'main', url: 'https://github.com/dipali-coditas/hello-wolrd.git' 
      }
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
          sh """
            sudo rm /var/www/html/index.html || echo 'No file found'
            sudo cp index.html /var/www/html/
          """  
        }
      }
    }
  }
}