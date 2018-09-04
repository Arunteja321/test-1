pipeline {
    agent any
    stages {
        stage('Example') {
            environment { 
                SECRET = credentials('s3-upload-authorizedUser') 
            }
            steps {
                wrap([$class: 'BuildUser']) {
                    echo env.BUILD_USER_ID
                }
                echo "secret is %SECRET%"
            }
        }
    }
}
