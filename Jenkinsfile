pipeline {
    agent any
    
    stages {
        stage ('Checkout') {
            steps {
                cleanWs()
                bat "git clone https://github.com/sokid93/JenkinsDotNet.git ."
            }
        }
        
        stage('Restore') {
            steps {
                bat "dotnet restore"
            }
        }
        stage ('Test') {
            steps {
                bat "dotnet test --configuration Release --logger trx --results-directory TestResults"
            }
        }
    }
}
