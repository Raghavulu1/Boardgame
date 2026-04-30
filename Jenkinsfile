pipeline {
    agent any
    
    tools {
        maven 'Maven 3.6'
        jdk 'jdk17'
    }
    
    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Raghavulu1/Boardgame.git'
            }
        }
        stage('Compile') {
            steps {
            sh 'mvn compile'
            }
        }
        stage('test') {
            steps {
                sh 'mvn test'
            }
        }
         stage('Package') {
            steps {
                sh 'mvn package'
            }
         }
          stage('Check') {
            steps {
                echo 'Hello world'
            }
         }
    }
}
