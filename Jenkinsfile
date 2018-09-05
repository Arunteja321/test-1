def buildUserId
def authorizedUserId
pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                wrap([$class: 'BuildUser']) {
                    script {
                        buildUserId = env.BUILD_USER_ID
                    }
                }
                withCredentials([string(credentialsId: 'authorizedUser', variable: 'user')]) {
                    script {
                        authorizedUserId = user
                    }
                }
                echo buildUserId
                echo authorizedUserId
            }
           
        }
    }
}
