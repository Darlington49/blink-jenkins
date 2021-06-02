pipeline {
    agent  any
  
    stages {
        stage('build') {
            steps {
              //  sh 'chmod u+x my_script.sh $IDF_PATH/export.sh'
              //  sh 'sudo $IDF_PATH/export.sh'
                sh 'ls'
                sh 'sudo docker run --rm -v $PWD:/project -w /project espressif/idf idf.py build'
            }
        }
    }
}
