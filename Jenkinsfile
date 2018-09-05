pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                wrap([$class: 'BuildUser']) {
                    echo env.BUILD_USER_ID
                    script {
                        def buildUserId = env.BUILD_USER_ID
                    }
                }
                withCredentials([string(credentialsId: 'authorizedUser', variable: 'user')]) {
                    echo user
                    script {
                        def authorizedUserId = user
                    }
                }
                script {
                    echo buildUserId
                    echo authorizedUserId
                }
            }
           
        }
    }
}
