pipeline {
    agent any

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
        steps('Deploy'){
            steps{
                echo 'Deploy the code'
            }
        }
    }
}