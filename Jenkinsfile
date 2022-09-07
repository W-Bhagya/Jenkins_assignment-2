pipeline {
    agent any 
        
        environment {
            def username = "Bhagya"

          //  USER_NAME = "bhagya"
            USER_ID = 101
            
        }
        
        stages {
            stage('Build') {
                steps {
                    echo "BUILD_NUMBER = ${env.BUILD_NUMBER}" 
                    sh 'echo BUILD_NUMBER = $BUILD_NUMBER'
                    
                }
            }
            
            stage('Test') {
                steps {
                    echo "Testing"
                    echo "Current user is ${username}"
                    echo "Current user ID is ${env.USER_ID}"
                    
                }
            }
            
            stage('Deploy') {
                steps {
                    echo "Deploying"
                   
                }
            }
        }
    
}
