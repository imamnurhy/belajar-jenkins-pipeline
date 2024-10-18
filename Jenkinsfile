pipeline{
    agent {
        node {
            label "docker && jdk17"
        }
    }
    
    stages {
        stage('Build') {
           steps {
                echo("Hello Build 1")
                echo("Hello Build 2")
                echo("Hello Build 3")
           }
        }
        stage('Test') {
           steps {
                echo("Hello Test 1")
                echo("Hello Test 2")
                echo("Hello Test 3")
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