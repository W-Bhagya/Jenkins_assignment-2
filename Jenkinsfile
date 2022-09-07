pipeline {
    agent any 
        
        environment {
            def user_name = "Bhagya"
            def user_id = 101
            
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
                    echo "Current user is ${user_name}"
                    echo "Current user ID is ${user_id}"
                    
                }
            }
            
            stage('Deploy') {
                steps {
                    echo "Deploying"
                   
                }
            }
        }
    
}
