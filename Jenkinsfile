pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''
                wget https://tomcat.apache.org/tomcat-6.0-doc/appdev/sample/sample.war
                '''
            }
        }
    }
}
