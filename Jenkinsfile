pipeline {
    agent any
    environment {
        buildUserId = 'buildUserId'
        authorizedUserId = 'authorizedUserId'
    }
    stages {
        stage('Example') {
            steps {
                wrap([$class: 'BuildUser']) {
                    echo env.BUILD_USER_ID
                    script {
                        env.buildUserId = env.BUILD_USER_ID
                    }
                }
                withCredentials([string(credentialsId: 'authorizedUser', variable: 'user')]) {
                    script {
                        env.authorizedUserId = user
                    }
                }
                echo env.buildUserId
                echo env.authorizedUserId
            }
           
        }
    }
}
