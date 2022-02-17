pipeline {
    agent any
    stages{
        stage('Branch name') {
            when {
                changeRequest branch: "develop"
            }
            steps {
                echo "${GIT_BRANCH.split("origin/")[1]}"
            }
        }
    }
}
