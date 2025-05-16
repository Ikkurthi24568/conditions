pipeline{
    agent any
     environment{        
        //DEPLOY_TO = 'production' //just an environment varible
         DEPLOY_TO = 'nonproduction'
    }
    stages{
        stage("Build"){
            steps{
                echo "Building the application"
            }
        }
        stage("anyOfStage"){
            when{
                anyOf{
                expression { BRANCH_NAME ==~ /(production|staging)/}
                environment name : 'DEPLOY_TO', value : 'production'
                }
            }
            steps{
                echo "Deploying K*s applications"
            }
        }
    }
}
