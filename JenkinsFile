//Running Parallel stages of testing on two agents
//Using Declarative syntax
pipeline{
    agent none
    stages{
        stage("Building")
        {
            agent {
            label "master"
            }
            steps{
                echo "Building"
            }
        }
        stage("Testing parallelly"){
            parallel{
                stage("test on linux1"){
                    agent{
                        label "master"
                    }
                    steps{
                        echo "testing on master"
                    }
                }
                stage("test on slave 1"){
                    agent{
                        label "slave-1"
                    }
                    steps{
                        echo "test on slave 1"
                    }
                }
            }
        }
    }
}