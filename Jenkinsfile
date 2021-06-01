pipeline {
    agent { docker { image 'espressif/idf:release-v4.1' } }
    stages {
        stage('build') {
            steps {
                sh 'ls'
                // sh 'idf.py build'
            }
        }
    }
}