node {
	stage('SCM Checkout') {
		git 'https://github.com/EugeneGrigorik/vaadinbank-master.git'
	}
	stage('Compile-Package'){
		def mvnHome = tool name: 'C:\\Program Files\\Maven\\apache-maven-3.6.1', type: 'maven'
		bat "cd D:/WorkspaceDocker/vaadinbank-master && mvn compile jib:build -DsendCredentialsOverHttp=true -Djib.httpTimeout=0 -Pproduction"
	}
}
