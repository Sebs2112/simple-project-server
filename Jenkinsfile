pipeline{
	agent any
        tools {
        maven 'Maven 3.6.2' 
    }
 stages {
        stage('Testing Environment') {
            steps {
                    sh 'mvn test -Dtest=ControllerAndServiceSuite'
		    sh 'mvn test -Dtest=IntegrationSuite'	
                }
            }
        stage('Build') {
            steps {
		         sh 'mvn package -DskipTests'
                 	 sh 'docker build -t="sebs2112/simple-project:latest" .'
                }
            }
        stage('Deploy') {
            steps {
		echo "Deploy"
            }
        }
   }
}

