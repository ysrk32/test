pipeline {
    agent any

    stages {
        stage('test') {
            steps {
                cleanWs deleteDirs: true, disableDeferredWipeout: true
                sh 'ls'
                checkout scm
                sh 'ls'
                echo 'abc'
            }
        }
    }
}
