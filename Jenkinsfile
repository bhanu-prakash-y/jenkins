pipeline {
    // agent section is used to define where the pipeline will run
    agent {
        node {
            label 'ROBOSHOP'
        }
    }
    // environment section is used to define environment variables that can be used throughout the pipeline
    environment {
        course = "DevOps"
    }
    options {
        disableConcurrentBuilds()   
  }
    stages {
        stage('Build') {
            steps {
                script{
                    sh """
                        echo "Building"
                        echo $course
                        sleep 5
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
