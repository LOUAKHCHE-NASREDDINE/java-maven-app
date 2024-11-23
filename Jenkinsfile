def gv

pipeline {
    agent any
    tools {
        maven 'Maven'
    }
    stage('test') {
            steps {
                script {
                    echo "Testing the application..."
                    sh 'mvn test'
                }
            }
        }


    stages {
        stage('build jar') {
            when {
                expression {
                    BRANCH_NAME == 'master'
                }
            }
            steps {
                script {
                    echo "Building the application..."
                    sh 'mvn package'
                }
            }
        }
    }

    stages {
        stage('deploy') {
            when {
                expression {
                    BRANCH_NAME == 'master'
                }
            }
            steps {
                script {
                    echo "Deploying the application..."
                    sh 'mvn deploy'
                }
            }
        }
    }
    
}
