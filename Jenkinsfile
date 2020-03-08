apiVersion = "v1"
node {
	stage('Build') {
		echo env.PATH
		echo apiVersion
		bat 'mvn clean package'
	}
}