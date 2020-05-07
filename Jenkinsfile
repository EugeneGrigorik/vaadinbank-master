node {
	stage('SCM Checkout') {
		git 'https://github.com/EugeneGrigorik/vaadinbank-master.git'
	}
	stage('Compile-Package'){
		def mvnHome = tool name: 'apache-maven-3.6.1', type: 'maven'
		bat "cd ${mvnHome}/bin" "mvn compile jib:build -DsendCredentialsOverHttp=true -Djib.httpTimeout=0 -Pproduction"
	}
}
