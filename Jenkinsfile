pipeline {
    agent any
    
    tools {
        maven 'maven'
    }
    
    environment {
        SCANNER_HOME = tool 'sonar-scanner'
    }

    stages {
        stage('git checkout') {
            steps {
               git 'https://github.com/jayakumar145/maven-web-application.git'
            }
        }
        
        stage ('maven build war file'){
            steps {
                sh 'mvn clean package'
		      }

        }
    }
       
   
}
