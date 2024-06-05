pipeline {
    agent any
    
    tools {
        maven 'maven3'
        tool name: 'jdk17', type: 'jdk'
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
