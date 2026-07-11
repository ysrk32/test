pipeline {
    options {
        timestamps true
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
                    env.SCM_BRANCH = scmVars.GIT_BRANCH
                }
                sh 'echo $SCM_BRANCH'
            }
        }
    }
}
