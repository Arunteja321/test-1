pipeline {
    agent any
    stages {
        stage('Example') {
            environment { 
                SECRET = credentials('authorizedUser') 
            }
            steps {
                wrap([$class: 'BuildUser']) {
                    echo env.BUILD_USER_ID
                }
                echo %SECRET%
            }
        }
    }
}
