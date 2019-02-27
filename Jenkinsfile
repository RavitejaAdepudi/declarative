pipeline {
    agent any
    tools {
        maven 'apache-maven-3.5.3'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn mavewebappdemo/pom.xml clean package'
            }
        }
    }
}
