pipeline {
    agent any
    
    tools {
        maven 'maven'
    }
    
    trigger {
        githubPush()
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
