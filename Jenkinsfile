pipeline{
    agent any
    environment {
        NAME= "Dear Student"
        DIRECTORY_PATH = "~Assignment5.1"
        TESTING_ENVIRONMENT= "Name of Testing Environment is Student Assignment"
        PRODUCTION_ENVIRONMENT="Name of Production Environment is Sumi Verma"
    }
    stages{
        stage ('Build'){
            steps{
                echo "Fetching source code from: $DIRECTORY_PATH"
                echo "\n compile the code and generate any necessary artifacts"
                echo "\n Build has Started and Completed"
                bat '\n java -version'
            }
        }
        stage ('Test'){
            steps{
                echo "Unit Tests Started and Completed in Testing Environment $TESTING_ENVIRONMENT"
                echo "\n Integration Tests Started and Completed"
                echo "\n Test has Started and Completed"
            }
        }
        stage ('Code Quality Check'){
            steps{
                echo "Check the Code Quality"
                echo "\n Code Quality Check has Started and Completed"
            }
        }
        stage ('Deploy'){
            steps{
                echo "deploy the application to a testing environment $TESTING_ENVIRONMENT"
                echo "\n Deploy has Started and Completed"
            }
        }
        stage ('Approval'){
            steps{
                echo "Approval has Started"
                script{
                sleep 10
                }
                echo "Approval has Started and Completed"
            }
        }
        stage ('Deploy to Production'){
            steps{
                echo "$PRODUCTION_ENVIRONMENT"
                echo "$NAME, Deploy to Production has Started and Completed"
            }
        }
    }
}

