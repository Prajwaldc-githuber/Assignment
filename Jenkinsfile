pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Clone or download the application package (WAR file)
                https://github.com/AKSarav/SampleWebApp/raw/master/dist/SampleWebApp.war
                sh 'mvn clean package'
            }
        }
    }
}
