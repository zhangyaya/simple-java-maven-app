@Library(['piper-lib', 'piper-lib-os']) _

pipeline {
    agent none
    options {
        skipDefaultCheckout()
        timestamps()
    }
    stages {
        stage('Build') {
            steps {
               sapPiperStageCentralBuild script: this
            }
        }
    }
}
