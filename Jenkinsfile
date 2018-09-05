pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                wrap([$class: 'BuildUser']) {
                    echo env.BUILD_USER_ID
                    def buildUserId = env.BUILD_USER_ID
                }
                withCredentials([string(credentialsId: 'authorizedUser', variable: 'user')]) {
                    echo user
                    def authorizedUserId = user
                }
                script {
                    echo buildUserId
                    echo authorizedUserId
                }
            }
           
        }
    }
}
