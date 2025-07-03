pipeline {  

    agent {

        node{
            label 'MAVEN'
            customWorkspace '/var/jenkins_home/workspace/maven-web-app'
        }
    }
        
    tools{
        maven "Maven-3.9.9"
    }
    stages {
        stage('Clone') {
            steps {
               git 'https://github.com/teju2707/maven-web-app-002.git'
            }
        }
        stage('Build') {
            steps {
               sh 'mvn clean package'
            }
        }
    }
}
