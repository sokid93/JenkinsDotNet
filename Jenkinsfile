pipeline {
    agent any
    
    stages {
        stage ('Checkout') {
            steps {
                cleanWs()
                bat "git clone https://github.com/sokid93/JenkinsDotNet.git ."
            }
        }
        stage ('Test') {
            steps {
                bat "dotnet test --configuration Release --no-build --logger trx --results-directory TestResults"
            }
        }
    }
}
