def buildUserId
def authorizedUserId
pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                wrap([$class: 'BuildUser']) {
                    echo env.BUILD_USER_ID
                    buildUserId = env.BUILD_USER_ID
                }
                withCredentials([string(credentialsId: 'authorizedUser', variable: 'user')]) {
                    echo user
                    authorizedUserId = user
                }
                script {
                    echo buildUserId
                    echo authorizedUserId
                }
            }
           
        }
    }
}
