pipeline {
    options {
        buildDiscarder logRotator(numToKeepStr: '5')
    }
    agent { dockerfile true }
    stages {
        stage('Build') {
            steps {
                sh 'cmake'
                sh 'cmake --build'
            }
        }
    }
}
