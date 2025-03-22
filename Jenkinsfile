pipeline{
    agent any
    environment{
        user = 'naveen'
        password = 'password'
    }
    stages{
        stage('acessing user and pass3ord'){
            parallel{
                stages{
                    stage('access user'){
                        steps{
                        sh 'echo ${user}'
                        sh 'sleep 60'
                        }
                    }
                    stage('accessing pwd'){
                        steps{
                            sh 'echo ${password}'
                            sh 'sleep 30'
                        }

                    }
                }
            }
        }
    }

}