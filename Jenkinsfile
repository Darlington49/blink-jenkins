pipeline {
    agent { 
        docker { 
            image 'espressif/idf:release-v4.1'
            args '--entrypoint='
        } 
    }
    stages {
        stage('build') {
            steps {
                sh '$IDF_PATH/export.sh'
                sh 'ls'
                sh 'idf.py build'
            }
        }
    }
}
