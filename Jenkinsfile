pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                wrap([$class: 'BuildUser']) {
                    echo env.BUILD_USER_ID
                }
                withCredentials([secretText(credentialsId: 'authorizedUser', secretVariable: 'SECRET')]) {
                       echo "secret is $SECRET"
                }
            }
        }
    }
}
