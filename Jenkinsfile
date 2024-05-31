pipeline {
    agent {
        node {
            label 'agent-1'
        }
    }

    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    options {
        timeout(time: 1, unit: 'HOURS') 
        disableConcurrentBuilds()
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

    stage('params') {
            steps {
                echo "Hello ${params.PERSON}"

                echo "Biography: ${params.BIOGRAPHY}"

                echo "Toggle: ${params.TOGGLE}"

                echo "Choice: ${params.CHOICE}"

                echo "Password: ${params.PASSWORD}"
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