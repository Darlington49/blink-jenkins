pipeline {
    agent  any
  
    stages {
        stage('build') {
            steps {
              //  sh 'chmod u+x my_script.sh $IDF_PATH/export.sh'
              //  sh 'sudo $IDF_PATH/export.sh'
                sh 'ls'
                sh 'docker run --rm -v $PWD:/project -w /project espressif/idf:release-v4.1 idf.py build'
            }
        }
    }
}
