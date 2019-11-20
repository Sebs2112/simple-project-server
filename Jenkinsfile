pipeline{
	agent any

environment {
    VERSION = readMavenPom().getVersion()
}

 stages {
	stage('version'){
	    steps{
		echo "${VERSION}" 
	}}
        stage('test'){
	}
	stage('build'){
	}
	stage('Deploy'){
	}
	stage('Testing env'){
	}
	stage('Staging'){
		when{
			expression{
				env.BRANCH_NAME == 'developer'
			}
		}
		steps{echo "staging"}
	}
	stage('Production'){
	when{
	expression{
		env.BRANCH_NAME == 'master'
}
}steps{
echo "production"
}	
}
}}

