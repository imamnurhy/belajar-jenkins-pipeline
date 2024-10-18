pipeline{
    agent {
        node {
            label "docker && jkd17"
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