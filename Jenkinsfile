pipeline {
    agent any
    stages{
        stage('Branch name') {
            when {
                changeRequest target: "develop"
            }
            steps {
                echo "${GIT_BRANCH.split("origin/")[1]}"
            }
        }
    }
}
