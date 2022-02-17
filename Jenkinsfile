pipeline {
    agent any
    stages{
        stage('Branch name') {
            anyOf {
                changeRequest()
                branch BRANCH_MAIN
            }
            steps {
                echo "${GIT_BRANCH.split("origin/")[1]}"
            }
        }
    }
}
