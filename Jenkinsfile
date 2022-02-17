pipeline {
    agent any
    stages{
        stage('Branch name') {
            when {
                expression {
                    return env.BRANCH_NAME != 'master';
                }
            }
            steps {
                echo "${GIT_BRANCH}"
            }
        }
    }
}
