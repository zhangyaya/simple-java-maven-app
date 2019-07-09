@Library(['piper-lib', 'piper-lib-os']) _

pipeline {
    agent {
            docker 'maven:3.6.1'}
    stages {
        stage('Init') {
            steps {
                library 'piper-lib-os'
                sapPiperStageInit script: this, customDefaults: params.customDefaults
            }
        stage('Build') {
            steps {
               sapPiperStageCentralBuild script: this
            }
        }
    }
}
