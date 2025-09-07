pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Clone or download the application package (WAR file)
                git branch: 'main',
                    credentialsId: 'your-credentials-id',
                    url: 'https://github.com/Prajwaldc-githuber/hello-world-war-java.git'
                sh 'mvn clean package'
            }
        }
    }
}
