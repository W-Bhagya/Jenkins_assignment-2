pipeline {
    agent any 
        
        environment {
            def user_name = "Bhagya"
            def user_id = 101
            def buildNumber = "currentBuild.number"
            
        }
        
        stages {
            stage('Build') {
                steps {
                    echo "Current Build Number = ${currentBuild.number}" 
                 
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
                    sh '20.197.30.191:443'
                    echo "Successfully Deployed"
                   
                }
            }
        }
    
}
