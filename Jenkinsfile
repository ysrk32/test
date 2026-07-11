pipeline {
    agent any

    stages {
        stage('test') {
            steps {
                sh 'ls'
                checkout scm
                sh 'ls'
                echo 'abc'
            }
        }
    }
}
