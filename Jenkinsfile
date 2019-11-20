
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
                steps{
                    echo "test"
                }
            }
            stage("build"){
                steps{
                  echo "build"
                }
            }
            stage("Deploy"){
                steps{
                  echo "deploy"
                }
            }
            stage("Testing env"){
                steps{
                  echo "test env"
                }
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
