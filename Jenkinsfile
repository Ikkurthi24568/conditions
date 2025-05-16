pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                echo "building app"
            }
        }
        stage('Sonar'){
            steps{
                echo "Scaning app"
            }
        }
         stage('DockerBuild'){
            steps{
                echo "Building container app"
            }
        }
         stage('Dockerpush'){
            steps{
                echo "Pushing the image"
            }
        }
         stage('DeployToDev'){
            steps{
                echo "Deploying the application to dev env"
            }
        }
         stage('DeployToDev'){
            steps{
                echo "Deploying the application to Test env"
            }
        }
        stage('DeployToStage'){
            when {
                branch 'release/*'
            }
            steps{
                echo "Deploying the application to Stage env"
            }
        }
        stage('DeployToProd'){
            when{
                tag pattern: "v\\d{1,2}\\.\\d{1,2}\\.\\d{1,2}", comparator: "REGEXP"
            }
            steps{
                echo "Deploying the application to Stage env"
            }
        }
    }
}
