pipeline {
    agent any
    options {
        buildDiscarder logRotator(numToKeepStr: '5')
    }
    stages {
        stage('Build') {
            cmakeBuild {
                sourceDir: 'src'
                buildDir: 'build'
                installation: 'InSearchPath'
            }
			sh './main'
        }
    }
}
