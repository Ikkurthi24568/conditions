pipeline{
    agent any
    parameters{
        string (name : 'CHANGE_TICKET', defaultValue: 'CH12345679' description: 'please enter chnage number')
        booleanParam (name: 'Is SRE Approve?' defaultValue: true, description: 'Is Approval taken from SRE')
        choice( name: 'RELEASE' choices: 'Regular\nHotfix', description: 'what Release is this')
        password(name: 'myPassword', defaultValue: '', description: "Enter the password")
    }
    stages{
        stage('Deploy to Dev') {
            steps{
                echo "Deploy to dev sucessfully!"
            }
        }
        stage('Deploy to prod'){
            steps{
                echo "Your chnage ticket ${params.CHANGE_TICKET} is validate"
                echo "Deploy to prod"
                echo "This is a ${params.RELEASE}"
                echo "The password is ${params.myPassword}"
            }
        }
    }
}
