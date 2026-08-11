pipeline {
     agent any 
        stages {
           stage('build') {
             steps {
                echo "building"
             }
           }   
        }
        stages {
            stage('test') {
                steps {
                    echo "testing"
      
                }
            }
        }
        stages {
            stage('deploy') {
                steps {
                    echo "deploying"
                }
            }        
        }
}








// pipeline {
//     // agent section is used to define where the pipeline will run
//     agent {
//         node {
//             label 'ROBOSHOP'
//         }
//     }
//     // environment section is used to define environment variables that can be used throughout the pipeline
//     environment {
//         course = "DevOps"
//     }
//     //options section is used to define options that can be applied to the entire pipeline
//     options {
//         disableConcurrentBuilds()
//         timeout(time: 5, unit: 'MINUTES') 
//   }
//     parameters {
//         string(name: 'BRANCH_NAME', defaultValue: 'main', description: 'Branch to build')
//         text(name: 'DEPLOY_ENV', defaultValue: 'dev', description: 'Deployment environment')
//         booleanParam(name: 'RUN_TESTS', defaultValue: true, description: 'Run tests after build')
//         choice(name: 'DEPLOY_STRATEGY', choices: ['blue-green', 'rolling', 'canary'], description: 'Deployment strategy')
//         password(name: 'NEXUS_PASSWORD', defaultValue: '', description: 'Nexus password')
//     }
//     stages {
//         stage('Build') {
//             steps {
//                 script{
//                     sh """
//                         echo "Building"
//                         echo $course
//                         sleep 5
//                     """
                    
//                 }
//             }
//         }
//         stage('Test') {
//             steps {
//                 script {
//                     sh """
//                         echo "Testing"
//                         echo "Hello ${params.PERSON}" 
//                         echo "Biography: ${params.BIOGRAPHY}"
//                         echo "Toggle: ${params.TOGGLE}"
//                         echo "Choice: ${params.DEPLOY}" 
//                         echo "Password: ${params.PASSWORD}"
//                     """
//                 }
//             }
//         }
//         stage('Deploy') {
//             /* input {
//                 message "shuold we continue with deployment?"
//                 ok "Deploy"
//                 submitter "admin"
//                 parameters {
//                     string(name: 'DEPLOY_ENV', defaultValue: 'dev', description: 'Deployment environment')
//                 }
//             } */
//             steps {
//                 script {
//                     sh """
//                         echo "Deploying"
//                     """
//                 }
//             }
//         }
//     }
//     // post build actions
//     post {
//         always {
//             echo "I always run"
//         }
//         success {
//             echo "I run only if the build succeeds"
//         }
//         failure {
//             echo "I run only if the build fails"
//         }
//     }
// }
