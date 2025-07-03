pipeline {
    agent {
        node {
            label 'MAVEN'
        }
    }
    environment {
        PATH = "/opt/maven/bin:$PATH"
    }
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/teju2707/maven-web-app-002.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean deploy -Djacoco.skip=true'
            }
        }
    }
}