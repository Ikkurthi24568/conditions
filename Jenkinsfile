//When : at least one condition must be specified
//if more than one codition is specified , all conditions must return true for the stage to be excuted

pipeline{

    agent any
    environment{
        DEPLOY_TO = 'production' //just an environment varible
    }
    
    stages{
        stage('WhenStage'){
            when{
                environment name : 'DEPLOY_TO', value : 'production'
            }
            steps {
                echo "Deploying to when stage"
            }
        }
    }
}
