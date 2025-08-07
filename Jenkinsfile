pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }

    environment {
        GREETING = 'Hello Jenkins'
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
        stage('Deploy') {
            steps {
                sh """
                    echo "Here I wrote shellscript"
                    env
                """
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
