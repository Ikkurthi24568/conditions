pipeline{
    agent any
    parameters{
        string(name: 'PERSON', defaultValue: 'siva', description: 'Enter your name')
    }
    stages{
        stage('ParametersExample'){
            steps{
                echo "Welcome ${params.PERSON}" //${params.key}
            }
        }
    }
}
