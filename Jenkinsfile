pipeline {
    agent any

    environment {
        // Set GOPATH to your workspace or Go directory (e.g., /Users/sumithb/go)
        GOPATH = "/Users/sumithb/go"

        // Enabling Go Modules
        GO111MODULE = "on"

        // Set GOROOT to the correct Go installation directory (without bin/go)
        GOROOT = '/opt/homebrew/opt/go/libexec'  // Adjusted GOROOT path
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout the repository from GitHub
                git url: 'https://github.com/Sumith-Bilamkar/go-jenkins-example.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                script {
                    // Build the Go application
                    sh 'go build -v'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Run Go tests
                    sh 'go test -v'
                }
            }
        }

        stage('Deploy') {
            steps {
                // Placeholder for actual deployment
                echo 'Deploying (this is just a placeholder for actual deployment)'
            }
        }
    }

    post {
        always {
            // Cleanup after the pipeline runs
            echo 'Cleaning up'
        }
    }
}