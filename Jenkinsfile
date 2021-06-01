pipeline {
    agent { 
        docker { 
            image 'espressif/idf:release-v4.1'
            args `--entrypoint='$IDF_PATH/export.sh'`
        } 
    }
    stages {
        stage('build') {
            steps {
              //  sh 'chmod u+x my_script.sh $IDF_PATH/export.sh'
              //  sh 'sudo $IDF_PATH/export.sh'
                sh 'ls'
                sh 'idf.py build'
            }
        }
    }
}
