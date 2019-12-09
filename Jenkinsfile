pipeline {
    agent any
        stages{
        stage('Build'){
            
            withMaven(jdk: 'java', maven: 'maven') {
    mvn clean package
} 
        }
                   
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
