def x = "***************************************************************************************"
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
                /*Same*/
                echo "${x}"
                echo "${GIT_BRANCH.split("origin/")[1]}"
                echo "${ghprbSourceBranch}"
                echo "${x}"
                echo "${ghprbTargetBranch}"
                echo "${x}"
            }
        }
    }
}
