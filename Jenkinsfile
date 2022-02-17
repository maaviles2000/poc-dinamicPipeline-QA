def x = "***************************************************************************************"
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
        when { 
            expression { return ghprbTargetBranch == 'master';}
            stage("Delete after #4"){
                steps{
                    echo "Do nothing!"
                }
            }
        }
        stage('Branch name') {
            when {

                expression {
                    return ghprbTargetBranch == 'master';
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
