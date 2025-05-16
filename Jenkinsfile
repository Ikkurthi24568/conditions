pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                echo "Building the applications"
            }
        }
        stage("DeployToProd"){
            when {
                //this stage should trigger if the branch is stage or production
                expression { BRANCH_NAME ==~/(production|staging)
                           }
            }
            steps{
                echo "deploying to production"
            }
        }
    }
}
