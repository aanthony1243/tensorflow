pipeline {
    agent { docker 'golang:1.7.3-alpine' }
    stages {
        stage('build') {
            steps {
                sh 'env.GOPATH=$PWD'
                sh 'mkdir -p $GOPATH/src/'
                dir('$GOPATH/src/') {
                    sh 'go version'
                    sh 'echo $GOPATH'
                }
            }

        }
    }
}