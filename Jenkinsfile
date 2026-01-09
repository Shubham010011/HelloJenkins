pipeline {
    agent any

    tools {
        jdk 'JDK8'
        maven 'Maven3'
    }

    stages {

        stage('Build') {
            steps {
                echo 'Building project using Maven'
                bat 'mvn clean package'
            }
        }
    }

    post {
        success {
            echo 'Maven build successful'
        }
        failure {
            echo 'Maven build failed'
        }
    }
}
