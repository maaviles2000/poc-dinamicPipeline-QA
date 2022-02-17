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
                echo "${GIT_BRANCH.split("origin/")[1]}"
                echo "${ghprbPullId}"
                echo "${ghprbActualCommit}"
                echo "${ghprbSourceBranch}"
            }
        }
    }
}
