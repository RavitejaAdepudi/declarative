pipeline {
    agent any
    tools {
        maven 'maven_3_5_0'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn mavewebappdemo/pom.xml clean package'
            }
        }
    }
}
