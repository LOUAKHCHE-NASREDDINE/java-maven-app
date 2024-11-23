pipeline {
    agent any // Use any available agent

    stages {
        stage('Test') {
            steps {
                script {
                    echo "Testing the application..."
                }
            }
        }

        stage('Build Jar') {
            when {
                branch 'master' // Ensure this stage runs only on the master branch
            }
            steps {
                script {
                    echo "Building the application..."
                }
            }
        }

        stage('Deploy') {
            when {
                branch 'master' // Ensure this stage runs only on the master branch
            }
            steps {
                script {
                    echo "Deploying the application..."
                }
            }
        }
    }
}
