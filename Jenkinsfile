pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Bluezzydev/simple-java-app.git'
            }
        }

        stage('Build') {
            steps {
                script {
                    try {
                        echo 'Building...'
                        sh 'echo "Building..."'
                    } catch (Exception e) {
                        echo 'Build failed!'
                        error('Build failed!')
                        throw e
                    }
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    if (env.BRANCH_NAME == 'feature') {
                        sh 'echo "Running tests..."'
                    } else {
                        sh 'echo "Skipping tests for non-feature branch."'
                    }
                }
            }
        }
    }
}

