pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'pes1ug22cs545-1'
                sh 'g++ ./main/hello.cpp -o hello_exec'
                sh 'chmod +x hello_exec'
            }
        }
        stage('Test') {
            steps {
                sh './hello_executerror'
            }
        }
        stage('Deploy') {
            steps {
                echo 'DEPLOYED!'
            }
        }
    }
    post {
        failure {
            error 'PIPELINE FAILED!'
        }
    }
}
