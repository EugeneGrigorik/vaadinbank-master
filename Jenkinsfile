node {
	stage('SCM Checkout') {
		git 'https://github.com/EugeneGrigorik/vaadinbank-master.git'
	}
	stage('Compile-Package'){
		def mvnHome = tool name: 'Jenkins-maven', type: 'maven'
		bat "${mvnHome}/bin/mvn compile jib:build -DsendCredentialsOverHttp=true -Djib.httpTimeout=0 -Pproduction"
	}
}
