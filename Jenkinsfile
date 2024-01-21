pipeline {
    agent any
    
    tools {
        jdk 'jdk11'
        maven 'maven3'
    }

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'feature-1', url: 'https://github.com/NicholasMariga/Petclinic-Learning-DevOps.git'
            }
        }
        
        stage('Compile') {
            steps {
                sh 'mvn clean compile -DskipTests=true'
            }
        }
        stage('Build Application') {
            steps {
                sh 'mvn clean package -DskipTests=true'
            }
        }
        
    }
}
