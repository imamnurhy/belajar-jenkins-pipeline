pipeline{
   agent none
    stages {
        stage('Prepare') {
            agent {
                node {
                    label "docker && jdk17"
                }
            }
           steps {
                echo("Start Job ${env.JOB_NAME}")
                echo("Start Build ${env.BUILD_NUMBER}")
                echo("Brannch Name ${env.BRANCH_NAME}")
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