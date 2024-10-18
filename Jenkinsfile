pipeline{
    agent {
        node {
            label "docker && jdk17"
        }
    }
    
    stages {
        stage('Build') {
           steps {
                echo("Hello Build")
           }
        }
        stage('Test') {
           steps {
                echo("Hello Test")
                sh("Error")
           }
        }
        stage('Deploy') {
           steps {
                echo("Hello Deploy")
           }
        }
    }
}