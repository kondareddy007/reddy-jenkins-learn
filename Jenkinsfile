pipeline {
    // agent none
    agent {
        node {
            label 'AGENT'
        }
    }
    triggers {
        cron ('H/30 * * * *')
    }
    environment {
        NAME = 'Kondareddy'
    }
    options {
        timeout(time: 1, unit: 'HOURS')
        disableConcurrentBuilds()
        ansiColor('xterm')
    }
    parameters {
        string (name: 'PERSON', defaultValue: 'prasanna', description: 'Who should i say hello to')
        text (name: 'BIOGRAPY', defaultValue: '', description: 'Enter some information about person')
        choice (name: 'choice', choices: ['DEV', 'QA', 'PROD'], description: 'pick any one')
        password(name: 'password', defaultValue: 'SECRET', description: 'ENTER a Password')
    }

    // tools {
    //     maven 'maven-3.9.9'
    //     jdk 'java-17'
    // }
    stages {
        stage('Build'){
            // agent {
            //     node {
            //         label 'AGENT'
            //     }
            // }
            input {
                message "Should we connect?"
                ok "Yes, We can connect"
                
            }
            steps{
                echo "testing stage level agent"
            
                sh """
                    echo "this is shell script"
                    echo "$NAME"
                    pwd
                    printenv
                    sleep 10
                """
                // Access parametres
                echo "Hello ${PERSON_NAME}, nice to meet you"
                // echo "Hello ${params.PERSON}"
                // echo "BIOGRAPHY ${params.BIOGRAPY}"
                // echo "choice ${params.choice}"
                // echo "Password is ${params.password}"
                
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