pipeline{
    agent any
     environment{        
        DEPLOY_TO = 'production' //just an environment varible
    }
    stages{
        stage("Build"){
            steps{
                echo "Building the application"
            }
        }
        stage("anyOdStage"){
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
