pipeline {
    agent { 
        docker { 
            image 'espressif/idf:release-v4.1'
            args '-v $PWD:/project -w /project --entrypoint=/bin/sh' 
        } 
    }
    stages {
        stage('build') {
            steps {
                sh 'ls'
                // sh 'idf.py build'
            }
        }
    }
}