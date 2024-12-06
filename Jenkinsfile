pipeline {
    agent {
        node {
            label 'AGENT'
        }
    }

    stages {
        stage('Build'){
            steps{
                echo "Building"
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