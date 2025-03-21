pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M98" and add it to the path.
        maven "M98"
    }

    stages {
        stage('Echo Version') {
            steps {
                sh 'echo version of the maven'
                sh 'mvn -version'
            }
        }
        stage('create repo'){
            steps{
                sh 'sudo mkdir  -p /home/jenkins/.m2/repository '
                sh 'sudo chmod 777 /home/jenkins/.m2/repository '
            }
        }
        stage('BUILD'){
            steps{
               git branch: 'main', url: 'https://github.com/Nkposa/jenkins-hello-world.git'
               
               sh "mvn clean package"
                
            }
        }
        stage('UNIT TESTS'){
            steps{
                sh "mvn test"
            }
        }
        
    
        
    }
}
