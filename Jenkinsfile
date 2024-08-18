pipeline{
    agent none
    stages{
        
        stage('Non-Parallel Stage'){
            agent{
                label "master"
            }
            steps{
                echo "This is stage will be executed first"
            }
        }
        
        stage('Run Tests'){
            parallel{
                stage('Test On Windows'){
                    agent{
                    label "WIndows_Node"
                    }
                    steps{
                    echo "Task1 on Agent"
                    }
                }
                
                stage('Test On Master'){
                    agent{
                    label "master"
                    }
                    steps{
                    echo "Task1 on master"
                    }
                }
            }
        }
    }
}
