pipeline {
    agent none

    stages {
        stage('Build') {
            agent {label 'tomcat-redhat'}
            steps {
                // Clone or download the application package (WAR file)
                    git clone https://github.com/Prajwaldc-githuber/hello-world-war-java.git
            }
        }
    }
}
