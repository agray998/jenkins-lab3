pipeline {
    agent any
    environment {
        PASSWORD = 'SuperSecret'
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('ls') {
            steps {
                sh "ls -alh"
            }
        }
        stage('create script') {
            steps {
                sh "echo 'echo hello from jenkins' | tee coolScript.sh" 
                sh "sh coolScript.sh"
            }
        }
    }
    post {
        always {
            archiveArtifacts 'coolScript.sh'
            cleanWs()
        }
    }
}
