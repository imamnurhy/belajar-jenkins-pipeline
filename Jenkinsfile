pipeline{
   agent none
    stages {
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