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
        stage('Deploy') {
            steps {
                sh '''
                scp sample.war ec2-user@172.31.45.119:/home/ec2-user/tomcat/webapps
                sudo rm sample.war
                '''
            }
        }
    }
}
