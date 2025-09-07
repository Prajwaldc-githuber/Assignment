pipeline {
    agent none

    stages {
        stage('Build') {
            agent { label 'tomcat-redhat' }
            steps {
                touch new_file
            }
        }
    }
}
