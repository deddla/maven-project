pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                 cmd /k  "mvn clean package"
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