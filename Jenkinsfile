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
           stage(checking stage variables){
                environment{
                    image = "alpine"
                    tag = "latest"
                }
                steps{
                    echo "image: ${image}"
                    echo "tag: ${tag}"

                }
           }

        }



}