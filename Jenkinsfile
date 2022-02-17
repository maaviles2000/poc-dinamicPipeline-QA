def originBranch = ghprbTargetBranch;
/* Can use *
echo "${GIT_BRANCH.split("origin/")[1]}"
echo "${ghprbSourceBranch}"
echo "${ghprbTargetBranch}"
*/
pipeline {
    agent any
    stages{
        stage("Delete after #1"){
            steps{
                echo "Do nothing!"
            }
        }
        stage("Delete after #2"){
            steps{
                echo "Do nothing!"
            }
        }
        stage("Delete after #3"){
            steps{
                echo "Do nothing!"
            }
        }
        stage('Branch name') {
            when {

                expression {
                    return originBranch == 'master';
                }
            }
            steps {
                echo "Do nothing!"
            }
        }
        stage('Branch name') {
            when {

                expression {
                    return originBranch == 'develop';
                }
            }
            steps {
                echo "Lets code in develop!"

            }
        }
    }
}
