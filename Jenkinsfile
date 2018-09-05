pipeline {
    agent any
    environment {
    }
    stages {
        stage('Example') {
            steps {
                wrap([$class: 'BuildUser']) {
                    echo env.BUILD_USER_ID
                }
                withCredentials([string(credentialsId: 'authorizedUser', variable: 'user')]) {
                    echo "My password is '%PW1%'!"
                }
            }
           
        }
    }
}
