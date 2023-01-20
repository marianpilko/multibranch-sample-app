pipeline {
    agent any
    options {
        buildDiscarder logRotator(numToKeepStr: '5')
    }
    stages {
        stage('Build') {
            agent {
                docker {
		    image 'cmake'
                }
            }
            steps {
                sh 'mkdir build'
		sh 'cd build'
		sh 'cmake ..'
		sh 'cmake --build .'
            }
        }
    }
}
