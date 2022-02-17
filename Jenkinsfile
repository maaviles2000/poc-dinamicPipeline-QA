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
                echo "${GITHUB_PR_TARGET_BRANCH}"
            }
        }
    }
}
