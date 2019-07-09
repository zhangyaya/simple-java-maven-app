@Library(['piper-lib', 'piper-lib-os']) _

pipeline {
    agent none
    options {
        skipDefaultCheckout()
        timestamps()
    }
    stages {
        stage('Init') {
            steps {
                library 'piper-lib-os'
                sapPiperStageInit script: this, customDefaults: params.customDefaults
            }
        }
        stage('Build') {
            steps {
               sapPiperStageCentralBuild script: this
            }
        }
    }
}
