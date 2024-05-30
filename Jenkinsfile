pipeline {
    agent {
        node {
            label 'agent-1'
        }
    }
    stages {
        stage('Example') {
            steps {
                echo 'Hello World'
            }
        }

    stage('Manoj') {
            steps {
                echo 'Hello Manoj'
            }
        }
    }

    post { 
        always { 
            echo 'I will always say Hello again!'
        }

        failure {
            echo 'build was fail plz check once'
        }

        success{
            echo 'build was success'
        }
    }
}