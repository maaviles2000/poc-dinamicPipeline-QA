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
                echo 'run this stage - only if the branch name started with feature/'
            }
        }
    }
}
