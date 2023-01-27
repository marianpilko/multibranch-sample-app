pipeline {
    options {
        buildDiscarder logRotator(numToKeepStr: '5')
    }
    agent { dockerfile true }
    stages {
        stage('Build') {
            steps {
<<<<<<< HEAD
                sh 'mkdir build && cd build'
                sh 'cmake ..'
                sh 'cmake --build .'
=======
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
>>>>>>> 8912ad063841b323e63663d0bfbbbb2d992dd1a4
            }
        }
    }
}
