pipeline {
    agent any
    environment {
        DEPLOY_to = 'production'
    }
    stages {
        stage ('when') {
            when {
                environment name : 'DEPLOY_to' , value: 'production'

            }
            steps {
                echo "Deploying to when stage"
            }
        }
    }
}
