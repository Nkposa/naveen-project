pipeline{
    agent any
    environment {
        registry = "docker.io"
        username = "dockerhub_username"
        password = "dockerhub_password"}
        stages{
           stage("checking env variables"){
            steps{
                echo "registry: ${registry}"
                echo "username: ${username}"
                echo "password: ${password}"
            }

           }
           stage('checking stage variables'){
                environment{
                    image = "alpine"
                    tag = "latest"
                    registry = "docker.io"
                }
                steps{
                    echo "image: ${image}"
                    echo "tag: ${tag}"
                    echo "registry: ${registry}"

                }
           }
           stage("checking Jenkins env variables"){
            steps{
                echo "JENKINS_HOME: ${JENKINS_HOME}"
                echo "JENKINS_URL: ${JENKINS_URL}"
                echo "BUILD_TAG: ${BUILD_TAG}"
                echo "BUILD_NUMBER: ${BUILD_NUMBER}"
                echo "JOB_NAME: ${JOB_NAME}"
                echo "BUILD_ID: ${BUILD_ID}"
                echo "BUILD_DISPLAY_NAME: ${BUILD_DISPLAY_NAME}"
                echo "BUILD_URL: ${BUILD_URL}"
                echo "EXECUTOR_NUMBER: ${EXECUTOR_NUMBER}"
                echo "NODE_NAME: ${NODE_NAME}"
                echo "WORKSPACE: ${WORKSPACE}"
                
            }
           }

        }



}