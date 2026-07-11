pipeline {
    agent any

    stages {
        stage('test') {
            steps {
                sh 'ls'
                scm checkout
                sh 'ls'
                echo 'abc'
            }
        }
    }
}
