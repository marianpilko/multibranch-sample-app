pipeline {
    agent any
    options {
        buildDiscarder logRotator(numToKeepStr: '5')
    }
    stages {
        stage('Build') {
	    steps {
                cmakeBuild clearnBuild: true, installation: 'InSearchPath', buildDir: 'build', steps: [[withCmake: true]]
	    }
        }
    }
}
