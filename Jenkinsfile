pipeline{
    agent {
        node {
            label "docker && jdk17"
        }
    }
    
    stages {
        stage('Build') {
           steps {
                echo("Start Build")
                sh("./mvnw clean compile test-compile")
                echo("Finins Build")
           }
        }
        stage('Test') {
           steps {
                echo("Start Test")
                sh("./mvnw test")
                echo("Finish Test")
           }
        }
        stage('Deploy') {
           steps {
                echo("Hello Deploy 1")
                echo("Hello Deploy 2")
                echo("Hello Deploy 3")
           }
        }
    }
}