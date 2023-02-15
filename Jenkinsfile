pipeline {
    agent any
    tools {
    maven "MAVEN3"
    jdk "OracleJDK8"
    }
    stages {
        stage('fetch source') {
            steps {
                git branch: 'paac', url: 'https://github.com/devopshydclub/vprofile-project.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn install'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
