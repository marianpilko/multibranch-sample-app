pipeline {
    agent any
    options {
        buildDiscarder logRotator(numToKeepStr: '5')
    }
    stages {
        stage('Build') {
	    steps {
                cmakeBuild cleanBuild: true, installation: 'InSearchPath', buildDir: 'build', steps: [[withCmake: true]]
	    }
        }
    }
}
