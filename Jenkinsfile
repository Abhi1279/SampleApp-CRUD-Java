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
        stage('Compile') {
            steps {
                
                sh 'mvn compile'
            }
        }
        // stage('Build') {
        //     steps {
        //         sh 'mvn clean package'
        //     }
        // }
        // stage('Test') {
        //     steps {
        //         sh 'mvn test'
        //     }
        //     post {
        //         always {
        //             junit '**/target/surefire-reports/*.xml'
        //         }
        //     }
        // }
        // stage('Package') {
        //     steps {
        //         archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
        //     }
        // }
        // Add deploy or other stages as needed
    }

    post {
        success {
            echo 'Build and tests succeeded!'
        }
        failure {
            echo 'Build or tests failed.'
        }
    }
}