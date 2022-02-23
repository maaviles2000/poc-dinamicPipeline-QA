pipeline {
    agent any
    
    stages {

         stage('Releases') {
            when {
                expression {
                    return targetBranch == 'master';
                }
            }
            steps {
                echo "**** MASTER ****"
                build job: 'Test'
            }

            when {
                expression {
                    return targetBranch == 'develop';
                }
                steps {
                    echo "**** DEVELOP ****"
                }
            }
        }
    }
}
