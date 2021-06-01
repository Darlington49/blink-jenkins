pipeline {
    agent { docker { image 'espressif/idf:release-v4.1' } }
    stages {
        stage('build') {
            steps {
                sh 'npm --version'
                sh 'sudo docker run --rm -v $PWD:/project -w /project espressif/idf:release-v4.1 idf.py build'
            }
        }
    }
}