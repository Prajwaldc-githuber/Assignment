pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'wget https://tomcat.apache.org/tomcat-6.0-doc/appdev/sample/sample.war -O sample.war'
            }
        }
        parallel {
        stage('Deploy1') {
            steps {
                sshagent(['ec2-ssh-key']) {
                    sh '''
                        scp -o StrictHostKeyChecking=no sample.war ec2-user@172.31.45.119:/home/ec2-user/tomcat/webapps/
                    '''
                }
            }
        }
        stage('Deploy2') {
            steps {
                sshagent(['ec2-ssh-key']) {
                    sh '''
                        scp -o StrictHostKeyChecking=no sample.war ubuntu@172.31.46.100:/opt/tomcat/tomcat10/webapps
                    '''
                }
            }
        }   
    }
}
