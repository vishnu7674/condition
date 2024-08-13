pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                echo "***** Building the application"
            }
        }
        stage ('Sonar') {
            steps {
                echo "***** Building the application"
            }
        }
        stage ('Dockerbuild') {
            steps {
                echo "***** Building the container application"
            }
        }
        stage ('DockerPush') {
            steps {
                echo "***** Pushing the image ********"
            }
        }
        stage ('Deploytodev') {
            steps {
                echo "***** Deploying  the application to dev env*******"
            }
        }
        stage ('Deploytotest') {
            steps {
                echo "***** Deploying  the application to dev test*******"
            }
        }
        stage ('Deploytostage') {
            when {
                branch "release/*"
            }
            steps {
                echo "***** Deploying  the application to stage env*******"
            }
        }
        stage ('Deploytoprod') {
            when {
                // our application should deploy to prod only if the app is going to though tag
                //vx.x.x == v1.2.3
                tag pattern: "v\\d{1,2}\\.\\d{1,2}\\.\\d{1,2}", comparator: "REGEXP"
            }
            steps {
                echo "***** Deploying  the application to prod env*******"
            }
        }
    }
}
