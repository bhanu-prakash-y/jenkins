pipeline {
    agent {
        node {
            label 'ROBOSHOP'
        }
    }
    environment {
        course = "DevOps"

    }
    stages {
        stage('Build') {
            steps {
                script{
                    sh """
                        echo "Building"
                        echo $course
                    """
                    
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh """
                        echo "Testing"
                    """
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    sh """
                        echo "Deploying"
                    """
                }
            }
        }
    }
    // post build actions
    post {
        always {
            echo "I always run"
        }
        success {
            echo "I run only if the build succeeds"
        }
        failure {
            echo "I run only if the build fails"
        }
    }
}
