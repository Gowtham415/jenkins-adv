pipeline{
    agent any
    environment{
        NEW_VERSION='1.3.0'
    }
    stages{
        stage("Build"){
            when{
                expression{
                    BRANCH_NAME='dev' && CODE_CHANGES=true
                }
            }
            steps{
                echo "This is build phase"
                echo "this is the version ${NEW_VERSION}"
            }
        }

        stage("Test"){
            while{
                expression{
                    BRANCH_NAME='dev' || BRANCH_NAME='master'
                }
            }
            steps{
                echo "This is test phase"
            }
        }

        stage("Deploy"){
            steps{
                echo "This is deploy phase"
            }
        }

    }
}
