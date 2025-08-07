pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
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
