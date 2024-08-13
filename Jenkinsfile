pipeline {
    agent any
    parameters {
        string(name: 'person', defaultValue: 'Vishnu', description: 'Enter your name')
    }
    stages {
        stage ('parameters example') {
            steps {
                echo " Welcome ${params.person}"
            }
        }
    }
}
