pipeline {
    agent any
    options {
        buildDiscarder logRotator(numToKeepStr: '5')
    }
    stages {
        stage('Build') {
	    steps {
                cmakeBuild installation: 'InSearchPath', steps: [[withCmake: true]]
	    }
        }
    }
}
