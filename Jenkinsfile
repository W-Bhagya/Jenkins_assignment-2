pipeline {
    agent any
    
    environment { 
        CC = 'clang'
    }

    stages {
        stage('Build') {
            environment { 
                DEBUG_FLAGS = '-g'
            }
            
            steps { 
                sh 'printenv' 
            }
        }
            
        stage('Test') {
            when {
                expression {
                    BRANCH_NAME = 'main'
                }
            }
            steps{
                echo 'Testing'
            }    
        }
        
        stage('Deploy') {
            steps{
                echo 'Deploying'
            }    
        }
    }
}
