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
                sh 'g++ -std=c++1y -g ./src/main.cpp -o main'
                sh './main'
            }
        }
    }
}
