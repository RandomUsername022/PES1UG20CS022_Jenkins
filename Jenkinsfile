pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'make -C /var/jenkins_home/workspace/PES1UG20CS022-1/main'
                echo 'Build Stage Successful'
            }
        }
        stage('Test') {
            steps {
                sh '/var/jenkins_home/workspace/PES1UG20CS022-1/main/hello_exec'
                echo 'Test Stage Successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
