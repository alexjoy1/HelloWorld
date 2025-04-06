pipeline {
    agent any

    tools {
        maven 'Maven'  // Must match the Maven name in Jenkins > Global Tool Config
    }

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/alexjoy1/HelloWorld.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
