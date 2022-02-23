def targetBranch = ghprbTargetBranch;
pipeline {
    agent any
    
    stages {
        stage('Releases'){
            stages {
                stage('Master') {
                    
                    when {
                        expression {
                            return targetBranch == 'master';
                        }
                    }
                    
                    steps {
                        echo "**** MASTER ****"
                        build job: 'Test'
                    }
                }
                
                stage('Develop') {
                   when {
                        expression {
                            return targetBranch == 'develop';
                        }
                    }
                    steps {
                        echo "**** DEVELOP ****"
                    } 
                }
            }
        }
    }
}
