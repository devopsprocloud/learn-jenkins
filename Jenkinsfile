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
}
