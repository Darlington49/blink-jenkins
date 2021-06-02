pipeline {
    agent  any
  
    stages {
        stage('build') {
            steps {
              //  sh 'chmod u+x my_script.sh $IDF_PATH/export.sh'
              //  sh 'sudo $IDF_PATH/export.sh'
                sh 'ls'
                sh 'docker run --rm --privileged -v $PWD:/project -w /project espressif/idf:release-v4.1 idf.py build'
            }
        }
        stage('flash') {
            steps {
              //  sh 'chmod u+x my_script.sh $IDF_PATH/export.sh'
              //  sh 'sudo $IDF_PATH/export.sh'
                sh 'ls'
                sh 'docker run --rm --privileged -v $PWD:/project -w /project espressif/idf:release-v4.1 openocd -f debug/ftdi_ft2322.cfg -f debug/esp-wroom-32.cfg -c "program_esp32 build/blink.bin 0x10000  verify exit;reset;shutdown;" '
            }
        }
    }
}
