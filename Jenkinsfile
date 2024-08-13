pipeline {
    agent any
    stages {
        stage ('build') {
            steps {
                echo "Building the application"
            }
        }
        stage ('deploytoprod') {
            when {
                // this stage should trigger if the branch is stage or production
                expression {BRANCH_NAME ==~ /(production|staging)/}
            }
            steps {
                echo "****** Deploying to production*****"
            }
        }
    }
}
