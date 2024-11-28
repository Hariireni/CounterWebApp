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
               deploy adapters: [tomcat9(credentialsId: 'tomcat', path: '', url: 'http://3.90.235.207:8090')], contextPath: '/java', war: '**/*.war'
            }
        }    
    }
}
code
