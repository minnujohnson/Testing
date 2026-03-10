pipeline {
    agent any

    stages {

        stage('Checkout') {
                steps {
                    git branch: 'main',
                        url: 'https://github.com/minnujohnson/Testing.git',
                        credentialsId: 'github-token'
                    }
                }

        stage('Run Tests') {
            steps {
                echo "Running test cases"
            }
        }

    }

    post {
        success {
            echo "Pipeline executed successfully"
        }
        failure {
            echo "Pipeline failed"
        }
    }
}
