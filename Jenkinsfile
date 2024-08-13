pipeline {
    parameters {
        string (name: 'CHANGE_TICKET', defaultValue: 'CH12345', description: please enter your change ticket)
        booleanParam (name: 'Is sre approved', defaultValue: true, description: 'is approval taken from sre')
        choice(choices: 'Regular\nHotfix', description: 'What release is this', name: 'Release')
        password(name: 'mypassword', defaultValue: '', description: 'Enter the password')
    }
    agent any
    stages {
        stage ('Deploy to dev') {
            steps {
                echo "Deployed to dev successfully"
            }
        }
        stage ('Deploy to prod') {
            steps {
                echo "Your change ticket ${params.CHANGE_TICKET} is validate"
                echo "Deploy to prod"
                echo "This is a ${params.Release}"
                echo "the password is ${params.mypassword}"
            }
        }
    }
}
