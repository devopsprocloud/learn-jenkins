pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }

    environment {
        GREETING = 'Hello Jenkins'
    }

    options {
        timeout(time: 1, unit: 'HOURS')
        disableConcurrentBuilds()
    }

    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello Prem..'
            }
        }
        stage('Hi') {
            steps {
                echo 'Hi Trixie...'
            }
        }
        stage('Hey') {
            steps {
                echo 'Hey from AGENT-1....'
            }
        }
        stage('Init') {
            steps {
                echo 'Initiating'
            }
        }
        stage('Deploy') {
            steps {
                    echo "Here I wrote shellscript"
                    echo "$GREETING"
            }
        }
        stage('Check Parameters') {
            steps {
                echo "Hello ${params.PERSON}"

                echo "Biography: ${params.BIOGRAPHY}"

                echo "Toggle: ${params.TOGGLE}"

                echo "Choice: ${params.CHOICE}"

                echo "Password: ${params.PASSWORD}"
            }
        }
    }
    //POST Stages
    post { 
        always { 
            echo 'Pipeline is executed'
        }
        failure {
            echo 'The pipeline is Failed, Please send some alerts'
        }
        success {
            echo 'Pipeline executed successfully'
        }
    }
}
