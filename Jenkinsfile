pipeline {
      agent any
    
    stages {
        stage("Maven Build") {
            steps{
                sh 'mvn clean install'
            }
        }  
        stage("tomcat deployment") {
            steps{
                deploy adapters: [tomcat9(credentialsId: '021b0d82-9cd9-4a06-bfbb-70cee88a9aa0', path: '', url: 'http://35.154.29.170:8090')], contextPath: '/devi', war: '**/*.war'
            }
        }    
    }
}
