pipeline {
    agent any 
    tools {
        maven 'maven-3.8.6'
    }
        
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

              
              stage('Deploy to tomcat server') {
                  
                  steps {
                      // deploy adapters: [tomcat9(credentialsId: 'cce3dde9-2fa9-41e0-b626-95fee22e7776', path: '', url: 'http://20.204.174.39:8080/')], contextPath: null, war: '**/*.war'   
                      
                     // deploy adapters: [tomcat9(url: 'http://20.204.174.39:8080/', credentialsId: 'tomcat_server')],war: 'target/*.war',contextPath: 'app'
                      // deploy adapters: [tomcat9(credentialsId: '64d2eb1f-a84a-4097-8063-3289ce7d5514', path: '', url: 'http://20.204.174.39:8080/')], contextPath: null, war: '**/*.war'
                  deploy adapters:[tomcat9(credentialsId:'tomcat_credential',path:'',url:'http://20.204.174.39:8080')],contextPath:'/pipeline',onFailure:false,war:'**/*.war'
                  }
                  
              }
     }
 }
              
