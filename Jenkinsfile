pipeline {
    agent any
    stages{
        stage('Branch name') {
            when {
                expression {
                    return CHANGE_TARGET == 'develop';
                }
            }
            steps {
                echo "${GIT_BRANCH.split("origin/")[1]}"
            }
        }
    }
}
