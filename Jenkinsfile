pipeline {
    agent any
    
    stages {
        
        stage('Build) {
              
              steps {
                  sh 'mvn clean package'
              }
              
              post {
                  success {
                      echo "Archiving the artifacts"
                      archiveArtifats artifacts: '**/target/*.war'
                  }
              }
         }
              
              stage('Deploy to tomcat server') {
                  
                  steps {
                      deploy adapters: [tomcat6(path: '', url: 'http://20.204.174.39:8080/')], contextPath: null, war: '**/.war*'
                  }
              }
     }
 }
              
