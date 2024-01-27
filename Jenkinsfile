pipeline {
    agent any

    stages {
        stage("Clone Code") {
            steps {
                echo "Cloning the code"
                git url: "https://github.com/dipali-coditas/notes-app-gcr.git", branch: "main"
            }
        }
    }
}
