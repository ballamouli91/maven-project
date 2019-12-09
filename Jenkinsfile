pipeline {
    agent any
    tools { 
        tool name: 'maven', type: 'maven' 
    }
    stages{
        stage('Build'){
            
            steps {
                sh 'mvn clean package'
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
