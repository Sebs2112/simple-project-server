pipeline{
        agent any

        environment {
            VERSION = readMavenPom().getVersion()
        }

        stages {
            stage("version"){
                steps{
                    echo "${VERSION}"
                }
            }
            stage("test"){
                echo "test"
            }
            stage("build"){
                echo "build"
            }
            stage("Deploy"){
                echo "deploy"
            }
            stage("Testing env"){
                echo "test env"
            }
            stage("Staging"){
                when{
                    expression{
                        env.BRANCH_NAME == 'developer'
                    }
                }
                steps{
                    echo "staging"
                }
           }
           stage('Production'){
                when{
                    expression{
                        env.BRANCH_NAME == 'master'
                    }
                }
                steps{
                    echo "production"
                }
          }
      }
}

