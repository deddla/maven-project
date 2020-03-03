pipeline {
    agent any
	
	environment {
		JAVA_HOME="C:/Users/sdeddla/applications/mulesoft/AdoptOpenJDK/jdk-8.0.242.08-hotspot"
		MAVEN_HOME="C:/Users/sdeddla/applications/apache/maven/apache-maven-3.6.3"
		PATH="%JAVA_HOME%/bin;%MAVEN_HOME%/bin;%PATH%;."
    }
    stages{
        stage('Build'){
            steps {
				 cmd "mvn clean package"
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