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
                sh 'chmod +x $IDF_PATH/export.sh'
                sh  '$IDF_PATH/export.sh'
                sh 'ls'
                sh 'idf.py build'
            }
        }
    }
}
