pipeline {
    
   agent any

    tools {
      maven 'maven3'
    }
    
    
    stages{
        stage ('Checkout') {
            steps{
                checkout poll: false, scm: scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/vcjain/docker-agent-demo.git']])
            }
            
        }
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
        stage('Deploy'){
            input {
              message 'Do you want to deploy build?'
              ok 'Yes I want'
              parameters {
                string description: 'Who is Approver?', name: 'Approver'
              }
            }
            steps{
                echo 'Deploying Build'
            }
        }
    }
}
