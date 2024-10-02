pipeline{
    agent any
    environment{
        NEW_VERSION='1.3.0'
    }
    stages{
        stage("Build"){
            when{
                expression{
                    BRANCH_NAME='main'
                }
            }
            steps{
                echo "This is the build phase"
                echo "this is the version ${NEW_VERSION}"
            }
        }

        stage("Test"){
            when{
                expression{
                    BRANCH_NAME='main' || BRANCH_NAME='master'
                }
            }
            steps{
                echo "This is the test phase"
            }
        }

        stage("Deploy"){
            steps{
                echo "This is deploy phase"
            }
        }

    }
}
