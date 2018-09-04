pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                wrap([$class: 'BuildUser']) {
                    echo "userId=%BUILD_USER_ID%,fullName=%BUILD_USER%,email=%BUILD_USER_EMAIL%"
                }
            }
        }
    }
}
