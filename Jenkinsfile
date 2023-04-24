node(){

	
	
	stage('Code Checkout'){
		checkout changelog: false, poll: false, scm: scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'GitHubCreds', url: 'https://github.com/sekhar-1995/MavenBuild.git']])
	}
	stage('Build Automation'){
		sh """
			ls -lart
			mvn clean install
			ls -lart target

		"""
	}
	
	
}
