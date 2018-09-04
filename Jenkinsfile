pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo 'Hello World'
                export STARTED_BY="`grep -i Started log`"
                echo "STARTED BY USER = %STARTED_BY%"
                export JUST_NAME="`echo "%STARTED_BY%" | sed "s@Started by user@@"`"
                echo "Jenkins User Name is %JUST_NAME%"
                echo %BUILD_USER_ID%
            }
        }
    }
}
