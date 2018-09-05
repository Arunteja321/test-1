pipeline {
    agent any
    environment {
        authorizedUser = credentials('authorizedUser')
    }
    stages {
        stage('Example') {
            steps {
                wrap([$class: 'BuildUser']) {
                    echo env.BUILD_USER_ID
                    echo env.authorizedUser
                }
            }
           
        }
    }
}
