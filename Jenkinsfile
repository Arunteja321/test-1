pipeline {
    agent any
    environment {
        //authorizedUser = credentials('authorizedUser')
    }
    stages {
        stage('Example') {
            steps {
                wrap([$class: 'BuildUser']) {
                    echo env.BUILD_USER_ID
                    //echo env.authorizedUser
                    //echo env.BUILT_USER_ID.equals(env.authorizedUser)
                }
                withCredentials([string(credentialsId: 'authorizedUser', variable: 'user')]) {
                    echo "My password is '%PW1%'!"
                }
            }
           
        }
    }
}
