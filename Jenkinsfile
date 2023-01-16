pipeline {
    agent any
    options {
        buildDiscarder logRotator(numToKeepStr: '5')
    }
    stages {
        stage('Build') {
            agent {
                docker {
                    image 'gcc'
                }
            }
            steps {
                sh 'gcc --version'
            }
        }
    }
}
