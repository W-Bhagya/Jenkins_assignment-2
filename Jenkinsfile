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
                    deploy adapters: [tomcat9(path: '', url: 'http://20.204.174.39:8080/')], contextPath: null, war: '**/.war*'
                    echo "Successfully Deployed"
                   
                }
            }
        }
    
}
