pipeline {
    agent any
    options {
        buildDiscarder logRotator(numToKeepStr: '5')
    }
    agent { dockerfile true }
    stages {
        stage('Build') {
            steps {
                sh 'mkdir build'
                sh 'cd build'
                sh 'cmake ..'
                sh 'cmake --build .'
            }
        }
    }
}
