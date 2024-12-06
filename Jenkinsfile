pipeline {
    agent none
    // agent {
    //     node {
    //         label 'AGENT'
    //     }
    // }

    stages {
        stage('Build'){
            agent {
                node {
                    label 'AGENT'
                }
            }
            steps{
                echo "testing stage level agent"
            }
        }
        stage('Tesing'){
            steps{
                echo "Testing"
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deploy the code'
            }
        }
    }
}