pipeline {
    agent any
	
	stages{
        stage('Build'){
            steps {
				 bat 'set PATH=%PATH%;C:/Users/sdeddla/applications/apache/maven/apache-maven-3.6.3/bin && java -version'
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