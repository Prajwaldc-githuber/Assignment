pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'wget https://tomcat.apache.org/tomcat-6.0-doc/appdev/sample/sample.war -O sample.war'
            }
        }

        stage('Deploy') {
            steps {
                sshagent(['ec2-ssh-key']) {
                    sh '''
                        scp -o StrictHostKeyChecking=no sample.war ec2-user@172.31.45.119:/home/ec2-user/tomcat/webapps/
                    '''
                }
            }
        }
    }
}
