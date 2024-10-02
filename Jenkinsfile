
pipeline{
    agent any

 parameters {
    string(name: 'VAR1', defaultValue:'Selenium', description: 'some description', trim: true)
    string(name: 'VAR2', defaultValue:'Jenkins', description: 'some description', trim: true)
     choice(name:'BROWSER', choices: ['CHROME', 'FIREFOX', 'SAFARI'], description: 'Select a browser')
}
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
                echo "This is the build phase ${params.VAR1} ${params.VAR2}"
                echo "this is the version ${NEW_VERSION}"
            }
        }

        stage("Test"){
            when{
                expression{
                    BRANCH_NAME='main'
                }
            }
            steps{
                echo "Tests are running in the browser ${params.BROWSER}"
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
