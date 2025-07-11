pipeline {
    agent any

    tools {

        // jdk 'jdk11' // Change to your JDK installation name
        // maven 'maven3' // Change to your Maven installation name
        maven 'mymvn' // Ensure 'mymvn' is configured in Jenkins tools

    }

    environment {
        // Define any environment variables here
        APP_NAME = 'SampleApp-CRUD-Java'
    }

    stages {
        stage('Git Checkout') {
            steps {
                git 'https://github.com/Abhi1279/SampleApp-CRUD-Java.git'
            }
        }
    }
    stage('Compile') {
        steps {
        sh 'mvn clean compile'
        }
    }

   
}