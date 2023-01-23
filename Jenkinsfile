pipeline {
    options {
        buildDiscarder logRotator(numToKeepStr: '5')
    }
    agent { dockerfile true }
    stages {
        stage('Build') {
            steps {
                //sh 'mkdir build && cd build'
                //sh 'ls -a'
                //sh 'cmake CMakeLists.txt'
                //sh 'cmake --build .'
                //sh './multibranch-sample-app'
                //sh './multibranch-sample-app-test'
                cmakeBuild installation: 'InSearchPath', steps[[withCmake: true]]
            }
        }
        stage('Test') {
            steps {
                ctest 'InSearchPath'
            }
        }
    }
}
