pipeline {
    agent any
    stages{
        stage('Build'){
            tool name: 'maven', type: 'maven'
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
