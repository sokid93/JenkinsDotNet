pipeline {
    agent any
    
    stages {
        stage ('Checkout') {
            steps {
                cleanWs()
                bat "git clone https://github.com/sokid93/JenkinsDotNet.git ."
            }
        }
    }
}
