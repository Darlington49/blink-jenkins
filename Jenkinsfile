pipeline {
    agent { docker { image 'node:14-alpine' } }
    stages {
        stage('build') {
            steps {
                sh 'ls'
                sh 'sudo docker run --rm -v $PWD:/project -w /project espressif/idf:release-v4.1 idf.py build'
            }
        }
    }
}