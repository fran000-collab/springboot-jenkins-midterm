pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/fran000-collab/springboot-jenkins-midterm.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvnw.cmd clean package'
            }
        }

        stage('Archive Artifact') {
            steps {
                archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
            }
        }

    }
}