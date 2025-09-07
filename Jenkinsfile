pipeline {
    agent none

    stages {
        agent { label 'tomcat-redhat' }
        stage('Build') {
            steps {
                sh '''
                git clone https://github.com/Prajwaldc-githuber/hello-world-war-java.git
                '''
            }
        }
    }
}
