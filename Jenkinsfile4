pipeline {
    agent any
    environment {
        user = 'naveen'
        password = 'password'
    }
    stages {
        stage('accessing user and password') {
            parallel {
                stage('access user') {
                    steps {
                        sh 'echo ${user}'
                        sh 'sleep 60'
                    }
                }
                stage('accessing pwd') {
                    steps {
                        sh 'echo ${password}'
                        sh 'sleep 30'
                    }
                }
            }
        }
    }
}