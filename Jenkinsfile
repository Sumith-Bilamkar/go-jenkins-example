pipeline {
    agent any

    environment {
        GOPATH = "${workspace}/go"
        GO111MODULE = "on"
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/Sumith-Bilamkar/go-jenkins-example.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                script {
                    sh 'go build -v'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh 'go test -v'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying (this is just a placeholder for actual deployment)'
            }
        }
    }

    post {
        always {
            echo 'Cleaning up'
        }
    }
}
