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
                deploy adapters: [tomcat9(credentialsId: 'tomcat', path: '', url: 'http://35.154.29.170:8090')], contextPath: 'hari', war: '**/*.war'
            }
        }    
    }
}
