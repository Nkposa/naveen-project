pipeline{
        agent any
        environment{
            servercreds = credentials('server-creds')
        }
        stages{
            stage('accessing creds'){
                steps{
                    sh '''
                    echo ${servercreds}
                    echo ${servercreds_USR}
                    echo ${servercreds_PSW}
                    echo ${servercreds_PSW}

                    '''

                }
            }





        }



}