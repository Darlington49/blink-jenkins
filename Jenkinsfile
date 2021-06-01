pipeline {
    agent { 
        docker { 
            image 'espressif/idf:release-v4.1'
             args '-v $PWD:/project -w /project ls' 
        } 
    }
    stages {
        stage('build') {
            steps {
                sh 'ls'
                sh 'docker run --rm -v $PWD:/project -w /project espressif/idf:release-v4.1 idf.py build'
            }
        }
    }
}