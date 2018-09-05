pipeline {
    agent any
    environment {
        buildUserId = 'buildUserId'
        authorizedUserId = 'authorizedUser
    }
    stages {
        stage('Example') {
            steps {
                wrap([$class: 'BuildUser']) {
                    echo env.BUILD_USER_ID
                    env.buildUserId = env.BUILD_USER_ID
                }
                withCredentials([string(credentialsId: 'authorizedUser', variable: 'user')]) {
                    env.authorizedUserId = user
                }
                echo env.buildUserId
                echo env.authorizedUserId
            }
           
        }
        stage('Deploy to Test') {
        }
    }
}
