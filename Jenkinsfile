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
