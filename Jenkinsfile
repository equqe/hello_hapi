#!/usr/bin/env groovy

pipeline {

    agent {
        dockerContainer {
            image 'node'
            args '-u root'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'building...'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'testing...'
                sh 'npm test'
            }
        }
    }
}
