pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Hello World'
                sh "sleep 30"
            }
        }
        stage('Test') {
            steps {
                sh "pwd"
                sh "ls -alh"
                sh "sleep 10"
            }
        }
        stage('Deploy') {
            steps {
                sh "touch file.txt"
                sh "mkdir foo"
                sh "mv file.txt foo"
                sh "ls -alh foo"
                sh "sleep 10"
            }
        }
    }
}
