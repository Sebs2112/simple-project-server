pipeline{
	agent any

 stages {
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

