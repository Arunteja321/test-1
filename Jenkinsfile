pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                wrap([$class: 'BuildUser']) {
                    echo env.BUILD_USER_ID
                }
                withCredentials([string(credentialsId: 'authorizedUser', variable: 'user')]) {
                    echo user
                }
            }
           
        }
    }
}
