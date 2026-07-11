pipeline {
    options {
        skipDefaultCheckout true
    }

    agent any

    stages {
        stage('clean') {
            steps {
                cleanWs deleteDirs: true, disableDeferredWipeout: true
            }
        }
        stage('checkout') {
            steps {
                script {
                    def scmVars = checkout scm
                    echo "scmVars = ${scmVars}"
                    echo "branch = ${scmVars.GIT_BRANCH}"
                    echo "commit = ${scmVars.GIT_COMMIT}"
                }
            }
        }
    }
}
