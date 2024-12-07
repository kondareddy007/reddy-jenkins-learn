pipeline {
    // agent none
    agent {
        node {
            label 'AGENT'
        }
    }
    environment {
        NAME = 'Kondareddy'
    }
    options {
        timeout(time: 1, unit: 'HOURS')
        disableConcurrentBuilds()
    }
    stages {
        stage('Build'){
            // agent {
            //     node {
            //         label 'AGENT'
            //     }
            // }
            steps{
                echo "testing stage level agent"
            
                sh """
                    echo "this is shell script"
                    echo "$NAME"
                    pwd
                    printenv
                    sleep 10
                """
                
            }

        }
        stage('Tesing'){
            steps{
                echo "Testing stage level testing"
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deploy the code stage level deploy'
            }
        }
    }

    post {
        always {
            echo 'it will always say hello again'
        }
        failure {
            echo " it will throw error message when build is failed"
        }
        success {
            echo "it will display when build when build is success"
        }
    }
}