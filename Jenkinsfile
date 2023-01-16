pipeline {
    agent any
    options {
        buildDiscarder logRotator(numToKeepStr: '5')
    }
    stages {
        stage('Stage 1') {
            steps {
                echo 'Hello world!' 
            }
        }
    }
}
