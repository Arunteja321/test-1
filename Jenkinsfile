pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                wrap([$class: 'BuildUser']) {
                    echo env.BUILD_USER_ID
                }
            }
            def data = credentials('authorizedUser')
        }
    }
}
