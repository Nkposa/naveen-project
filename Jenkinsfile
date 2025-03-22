pipeline {
    agent any
    parameters {
        string(name: 'environment', defaultValue: 'dev', description: 'Provide the environment')
        booleanParam(name: 'run_tests', defaultValue: true, description: 'Run tests if true')
    }
    stages {
        stage('access env params') {
            when {
                expression {
                    return params.run_tests == true
                }
            }
            steps {
                sh 'echo ${params.run_tests}'
            }
        }
        stage('deploy'){
            steps{
                sh 'echo ${params.environment}'
            }
        }
    }
}