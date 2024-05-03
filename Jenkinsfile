pipeline{
    agent any
    environment {
        NAME= "Dear Student"
        DIRECTORY_PATH = "~Assignment6.1"
        TESTING_ENVIRONMENT= "Name of Testing Environment is Student Assignment"
        PRODUCTION_ENVIRONMENT="Name of Production Environment is Sumi Verma"
    }
    stage ('Build'){
        steps{
            echo "Build has Started after Commit"
            script{
            sleep 10
            }
            echo "Fetching source code from: $DIRECTORY_PATH"
            echo "\n compile the code and generate any necessary artifacts"
            echo "\n Build has Started and Completed"
            bat '\n java -version'
            echo "\n Build Technologies: Grunt, Webpack, Maven, Nant, Gradle, NPM, SBT (Scala Build Tool)"
        }
        /*post{
            success{
                mail to: "forstudentassignments@gmail.com",
                subject: "Build Status Email",
                body: "Build was Successful"
            }
            failure {
                mail to: "forstudentassignments@gmail.com", 
                subject: "Build Status Email",
                body: "Build was not Successful"
            }*/
        }
    
    stage ('Unit and Integration Test'){
        steps{
            echo "Unit Tests Started and Completed in Testing Environment $TESTING_ENVIRONMENT"
            echo "\n Unit and Integration Tests Started and Completed"
            echo "\n Test Technologies: Selenium, Cypress, Protractor, EggPlant, Junit, Katalon, Apache JMeter, Test Complete, Appium, Ranorex Studio"
        }
        post{
            success{
                mail to: "forstudentassignments@gmail.com",
                subject: "Unit and Integration Test Status Email",
                body: "Unit and Integration Test were Successful"
            }
            failure {
                mail to: "forstudentassignments@gmail.com", 
                subject: "Unit and Integration Test Status Email",
                body: "Unit and Integration Test was not Successful"
            }
        }
    }
    stage ('Code Analysis'){
        steps{
            echo "Code Analysis"
            echo "\n Code Analysis has Started and Completed"
            echo "\n Code Analysis Technologies: SonarQube, ReSharper, CodeClimate, CAST"
        }
    }
    stage ('Security Scan'){
        steps{
            echo "Security Scan of the application"
            echo "\n Security Scan has Started and Completed"
            echo "\n Security Scan Technologies: GitLab SAST Support (Static Application,Security Testing), TerraForm, AWS CloudFormation"
        }
        post{
            success{
                mail to: "forstudentassignments@gmail.com",
                subject: "Security Scan Status Email",
                body: "BSecurity Scan was Successful"
            }
            failure {
                mail to: "forstudentassignments@gmail.com", 
                subject: "Security Scan Status Email",
                body: "Security Scan was not Successful"
            }
        }
    }
    stage ('Deploy to Staging'){
        steps{
            echo "Deploy to Staging the application"
            echo "\n DeployDeploy to Staging has Started and Completed"
            echo "\n Deploy to Staging Technologies: Jenkins, AWS Elastic Beanstalk, Heroku, Docker, GitLab, Kubernetes"
        }
    }
    stage ('Integration Tests on Staging'){
        steps{
            echo "Integration Tests on Staging"
            echo "\n Integration Tests on Staging has Started and Completed"
            echo "\n Integration Tests on Staging Technologies: GitLab, Heroku, Docker, Kubernetes, Jenkins"
        }
        post{
            success{
                mail to: "forstudentassignments@gmail.com",
                subject: "Integration Tests on Staging Status Email",
                body: "Integration Tests on Staging were Successful"
            }
            failure {
                mail to: "forstudentassignments@gmail.com", 
                subject: "Integration Tests on Staging Status Email",
                body: "Integration Tests on Staging was not Successful"
            }
        }
    }
    /*stage ('Approval'){
        steps{
            echo "Approval has Started"
            script{
            sleep 10
            }
            echo "Approval has Started and Completed"
        }
    }*/
    stage ('Deploy to Production'){
        steps{
            echo "$PRODUCTION_ENVIRONMENT"
            echo "$NAME, Deploy to Production has Started and Completed"
            echo "Deploy Technologies: AWSCodeDeploy, AWS CloudFormation, CodeCommit, Systems Manager, OpsWork"
        }
    }
}



