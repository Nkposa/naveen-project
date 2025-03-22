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
            stage('accessing creds using credentials method'){
                stage{
                    withCredentials = ([usernamePassword(credentialsId: 'server-creds'), usernameVariable = 'myuser', passwordVariable = 'mypwd'])
                    steps{
                        sh '''
                            echo my_user_nameis: ${myusr}
                            echo my_pwd: ${mypwd}
                            
                        '''
                    }
                }
            }





        }



}