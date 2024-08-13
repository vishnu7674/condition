pipeline {
    agent any
    environment {
        DEPLOY_to = 'production'
    }
    stages {
        stage ('build') {
            steps {
                echo "**** Builing the app"
            }
        }
        stage ('anyofstage') {
            when {
                // this stage should trigger if the branch is stage or production
                anyOf {
                    expression {BRANCH_NAME ==~ /(production|staging)/} //condition 1
                    environment name : 'DEPLOY_to' , value: 'production' //conditon 2
                }
            }
                
            steps {
                echo "Deploying the app"
            }
        }
    }
}
