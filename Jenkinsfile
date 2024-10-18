pipeline{
    agent none

    environment {
        AUTHOR = "Imam nurhidayat"
        EMAIL = "imamnurhy@gmail.com"
    }

    triggers {
        // cron("*/1 * * * *")
        pollSCM("*/1 * * * *")
    }

    stages {
        stage('Prepare') {

            environment {
                APP = credentials("imamkey");
            }

            agent {
                node {
                    label "docker && jdk17"
                }
            }
           steps {
                echo("Author ${AUTHOR}")
                echo("Email ${EMAIL}")
                echo("Start Job ${env.JOB_NAME}")
                echo("Start Build ${env.BUILD_NUMBER}")
                echo("Brannch Name ${env.BRANCH_NAME}")
                echo("App Username ${APP_USR}")
                echo("App Password ${APP_PSW}")
           }
        }
        stage('Build') {
            agent {
                node {
                    label "docker && jdk17"
                }
            }
           steps {
                echo("Start Build")
                sh("./mvnw clean compile test-compile")
                echo("Finins Build")
           }
        }
        stage('Test') {
            agent {
                node {
                    label "docker && jdk17"
                }
            }
           steps {
                echo("Start Test")
                sh("./mvnw test")
                echo("Finish Test")
           }
        }
        stage('Deploy') {
            agent {
                node {
                    label "docker && jdk17"
                }
            }
           steps {
                echo("Hello Deploy 1")
                echo("Hello Deploy 2")
                echo("Hello Deploy 3")
           }
        }
    }
}