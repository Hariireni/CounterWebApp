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
                deploy adapters: [tomcat9(credentialsId: 'admin', path: '', url: 'http://3.90.235.207:8090/')], contextPath: 'hari', war: '**/*.war'
            }
        }    
    }
}
code
