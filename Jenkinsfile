
pipeline {
    agent any


    
    
    tools {
        maven 'maven3'
        jdk 'jdk17'
    }
    
    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/jaiswaladi2468/BoardgameListingWebApp.git'
            }
        }

        stage('Unit Tests') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
