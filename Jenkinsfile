def x = "***************************************************************************************"
pipeline {
    agent any
    stages{
        stage('Branch name') {
            when {
                expression {
                    return ghprbTargetBranch == 'develop';
                }
            }
            steps {
                echo "Lets code in develop!"
                /*Same
                echo "${x}"
                echo "${GIT_BRANCH.split("origin/")[1]}"
                echo "${ghprbSourceBranch}"
                echo "${x}"
                echo "${ghprbTargetBranch}"
                echo "${x}"*/
            }
        }
    }
}
