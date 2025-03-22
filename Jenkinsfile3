pipeline {
    agent any
    environment {
        servercreds = credentials('server-creds')
    }
    stages {
        stage('accessing creds') {
            steps {
                sh '''
                echo ${servercreds}
                echo ${servercreds_USR}
                echo ${servercreds_PSW}
                '''
            }
        }
        stage('accessing creds using credentials method') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'server-creds', usernameVariable: 'myuser', passwordVariable: 'mypwd')]) {
                    sh '''
                    echo my_user_name is: ${myuser}
                    echo my_pwd: ${mypwd}
                    '''
                }
            }
        }
    }
}