pipeline {
    
   agent { dockerfile true }
    tools {
      maven 'maven3'
    }
    
    
    stages{
        stage ('Build') {
            steps {
                echo "Build Stage is in progress"
                sh 'mvn compile'
            }
            
        }
        stage ('Test'){
            steps {
                echo "Test Stage is in progress"
                sh 'mvn test'
            }
            
        }
    }
}
