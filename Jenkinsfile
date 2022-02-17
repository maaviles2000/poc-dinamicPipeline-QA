pipeline {
    agent any
    stages{
        stage('Branch name') {
            when {
                branch 'feature/*'
            }
            steps {
                echo 'run this stage - only if the branch name started with feature/'
            }
        }
    }
}
