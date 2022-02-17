def ramagithub, prdestino, prorigen
pipeline {
    agent any
    stages{
        stage('Branch name') {
            steps{
                script {
                    prdestino=env.GITHUB_PR_TARGET_BRANCH
                    prorigen=env.GITHUB_PR_SOURCE_BRANCH
                    ramagithub=env.GIT_BRANCH
                    ramagithub=ramagithub.split("origin/")[1]
                    echo env.GITHUB_PR_TARGET_BRANCH
                    echo env.GITHUB_PR_SOURCE_BRANCH
                    echo env.GIT_BRANCH
                    echo "${prdestino}"
                    echo "${prorigen}"
                    echo "${ramagithub}"
                    
                    switch(ramagithub) {
                        case "develop":
                            if (prorigen == 'develop' && prdestino== 'master') {
                                echo 'PR MASTER'
                            }
                            break
                        case "dani":
                            if (prorigen == 'dani' && prdestino== 'develop') {
                                echo 'PR DEVELOP'
                            }
                            break
                      default:
                            echo 'DEFAULT'
                            break
                        
                    }
                }
            }
        }
    }
}
