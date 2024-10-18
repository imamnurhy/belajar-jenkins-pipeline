pipeline{
    agent {
        node {
            label "docker && jdk17"
        }
    }
    
    stages {
        stage('Hello') {
           steps {
                echo("Hello Pipeline")
           }
        }
    }
}