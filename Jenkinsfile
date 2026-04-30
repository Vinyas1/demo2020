pipeline { 
    agent any 
 
    tools { 
        
        maven 'Maven3' 
    } 
 
    stages {
            stage('CHECKOUT') { 
            steps { 
            git branch: 'main', url: 'https://github.com/Vinyas1/demo2020.git'

                            } 
        } 
 
        stage('Build') { 
            steps { 
                dir('demo'){ 
                bat 'mvn clean install' 
            } 
            } 
        } 
        stage('Test') { 
            steps { 
                dir('demo'){ 
                bat 'mvn test' 
            } 
            } 
        } 
    }    
} 